---
description: FlashLiquidity core and periphery smart contracts derived from UniswapV2
---

# Smart contracts

FlashLiquidity is a binary smart contract system. [Core](smart-contracts.md#core) contracts provide fundamental safety guarantees for all parties interacting with FlashLiquidity. [Periphery](smart-contracts.md#periphery) contracts interact with one or more core contracts but are not themselves part of the core.

## Core <a href="#core" id="core"></a>

[Source code](https://github.com/Uniswap/uniswap-v2-core)

The core consists of a singleton [factory](smart-contracts.md#factory) and many [pairs](smart-contracts.md#pairs), which the factory is responsible for creating and indexing. These contracts are quite minimal, even brutalist. The simple rationale for this is that contracts with a smaller surface area are easier to reason about, less bug-prone, and more functionally elegant. Perhaps the biggest upside of this design is that many desired properties of the system can be asserted directly in the code, leaving little room for error. One downside, however, is that core contracts are somewhat user-unfriendly. In fact, interacting directly with these contracts is not recommended for most use cases. Instead, a periphery contract should be used.

### Factory <a href="#factory" id="factory"></a>

[Reference documentation](https://docs.uniswap.org/protocol/V2/reference/smart-contracts/factory)

The factory holds the generic bytecode responsible for powering pairs. Its primary job is to create one and only one smart contract per unique token pair. It also contains logic to turn on the protocol charge.

### Pairs <a href="#pairs" id="pairs"></a>

[Reference documentation](https://docs.uniswap.org/protocol/V2/reference/smart-contracts/pair)

[Reference documentation (ERC-20)](https://docs.uniswap.org/protocol/V2/reference/smart-contracts/Pair-ERC-20)

Pairs have two primary purposes: serving as automated market makers and keeping track of pool token balances. They also expose data which can be used to build decentralized price oracles.

## Periphery <a href="#periphery" id="periphery"></a>

[Source code](https://github.com/Uniswap/uniswap-v2-periphery)

The periphery is a constellation of smart contracts designed to support domain-specific interactions with the core. Because of FlashLiquidity's permissionless nature, the contracts described below have no special privileges, and are in fact only a small subset of the universe of possible periphery-like contracts. However, they are useful examples of how to safely and efficiently interact with FlashLiquidity.

### Library <a href="#library" id="library"></a>

[Reference documentation](https://docs.uniswap.org/protocol/V2/reference/smart-contracts/library)

The library provides a variety of convenience functions for fetching data and pricing.

### Router <a href="#router" id="router"></a>

[Reference documentation](https://docs.uniswap.org/protocol/V2/reference/smart-contracts/router-02)

The router, which uses the library, fully supports all the basic requirements of a front-end offering trading and liquidity management functionality. Notably, it natively supports multi-pair trades (e.g. x to y to z), treats MATIC as a first-class citizen, and offers meta-transactions for removing liquidity.

## Design Decisions <a href="#design-decisions" id="design-decisions"></a>

The following sections describe some of the notable design decisions made in FlashLiquidity. These are safe to skip unless you're interested in gaining a deep technical understanding of how FlashLiquidity works under the hood, or writing smart contract integrations!

### Sending Tokens <a href="#sending-tokens" id="sending-tokens"></a>

Typically, smart contracts which need tokens to perform some functionality require would-be interactors to first make an approval on the token contract, then call a function that in turn calls transferFrom on the token contract. This is _not_ how FlashLiquidity pairs accept tokens. Instead, pairs check their token balances at the _end_ of every interaction. Then, at the beginning of the _next_ interaction, current balances are differenced against the stored values to determine the amount of tokens that were sent by the current interactor. See the whitepaper for a justification of why this is the case, but the takeaway is that **tokens must be transferred to the pair before calling any token-requiring method** (the one exception to this rule is Flash Swaps).

### MATIC <a href="#matic" id="matic"></a>

Matic⇄ERC-20 pairs must be emulated with WMATIC. The motivation behind this choice was to remove Matic-specific code in the core, resulting in a leaner codebase. End users can be kept fully ignorant of this implementation detail, however, by simply wrapping/unwrapping Matic in the periphery.

The router fully supports interacting with any WMATIC pair via MATIC.

### Minimum Liquidity <a href="#minimum-liquidity" id="minimum-liquidity"></a>

To ameliorate rounding errors and increase the theoretical minimum tick size for liquidity provision, pairs burn the first MINIMUM\_LIQUIDITY pool tokens. For the vast majority of pairs, this will represent a trivial value. The burning happens automatically during the first liquidity provision, after which point the totalSupply is forevermore bounded.

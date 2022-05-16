---
description: FlashLiquidity protocol overview
---

# Protocol overview

FlashLiquidity protocol is based upon [uniswap-v2](https://github.com/Uniswap/v2-core) pools and charges a flat fee of 0.30% for token swap:

* 0.25% is distributed (proportionally) to liquidity providers.
* 0.05% is used to buy back and partially burn [FLIQ](fliq-token.md) tokens through the Incentivizer contract (derived from sushiswap [sushimaker](https://github.com/sushiswap/sushiswap/blob/canary/contracts/SushiMaker.sol) contract).

{% hint style="success" %}
Incentivizer contract burn all FLIQ tokens collected from FLIQ pairs fees while other tokens collected are converted and used to buy back and distribute FLIQ tokens to liquidity providers.
{% endhint %}

FLIQ tokens bought back with the Incentivizer contract are then distributed to Flashliquidity FLIQ/MATIC liquidity providers staking their FLIQ/MATIC LP tokens in the Flash Swaps Farm section.

The protocol’s key differentiator is that liquidity providers can earn both a 0.25% fee of the trading volume as well as the arbitrage profits associated with keeping a liquidity pool balanced.

Liquidity pairs can be left open for public trading _or_ assigned to a privileged address where a ‘FlashSwapper’ contract is deployed to handle the flash swaps execution logic and distribute arbitrage profits to liquidity providers. In the cases where a FlashSwapper contract is deployed, flash swaps can only be performed by an authorized address — blocking external arbitrageurs that could compete (through [frontrunning](https://arxiv.org/pdf/2102.03347.pdf)) with automated flash swaps executed by the FlashSwapper contract. This effectively makes it possible to distribute all arbitrage profits to liquidity providers instead of independent arbitrageurs.

Profits are distributed in one of the two token composing the FlashLiquidity pair in question (refered as Reward token).&#x20;

{% hint style="info" %}
example**:** MATIC-DAI pair distribute flashswaps profits in DAI.&#x20;
{% endhint %}

98% of the profits derived from flash swaps are distributed to liquidity providers staking their LP tokens in the Flash Swaps Farms section.

Currently 2% of the profits derived from flash swaps are kept by the protocol for gas fees repayment (FlashLiquidity pays for flash swaps gas fees in advance) , infrastructure maintenance, contests rewards and further expansion. &#x20;

{% hint style="info" %}
Currently Incentivizer is owned by FlashLiquidity developer.

Ownership will be transferred once [FLIQ](fliq-token.md) tokens will be enough distributed and decentralized governance begin.&#x20;
{% endhint %}


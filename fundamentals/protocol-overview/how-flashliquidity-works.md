---
description: FlashLiquidity protocol derived from uniswap-v2 pools
---

# How FlashLiquidity works

FlashLiquidity is an _automated liquidity protocol_ powered by a constant product formula and implemented in a system of non-upgradeable smart contracts on the [Polygon](https://docs.polygon.technology) blockchain prioritizing **decentralization**, **censorship resistance**, and **security**.

Each FlashLiquidity smart contract, or pair, manages a liquidity pool made up of reserves of two [ERC-20](https://eips.ethereum.org/EIPS/eip-20) tokens.

Anyone can become a liquidity provider (LP) for a pool by depositing an equivalent value of each underlying token in return for pool tokens. These tokens track pro-rata LP shares of the total reserves, and can be redeemed for the underlying assets at any time.

Pairs act as automated market makers, standing ready to accept one token for the other as long as the “constant product” formula is preserved. This formula, most simply expressed as `x * y = k`, states that trades must not change the product (`k`) of a pair’s reserve balances (`x` and `y`). Because `k` remains unchanged from the reference frame of a trade, it is often referred to as the invariant. This formula has the desirable property that larger trades (relative to reserves) execute at exponentially worse rates than smaller ones.

In practice, FlashLiquidity applies a 0.30% fee to trades (0.25% to liquidity providers, 0.05% to buy back, distribute and partially burn [FLIQ](../fliq-token.md)), which is added to reserves. As a result, each trade actually increases `k`. This functions as a payout to LPs, which is realized when they burn their pool tokens to withdraw their portion of total reserves.

{% hint style="success" %}
The **key difference** between **FlashLiquidity** and **Uniswap** is that token swap can only be performed by **authorized addresses** (FlashBot contracts).
{% endhint %}

Every FlashLiquidity pair is coupled with a FlashBot contract which periodically perform flash swaps (when prices diverges between FlashLiquidity and others Polygon markets) and distribute profits to liquidity providers instead of relaying on external arbitrageurs to help equalize prices across broader Polygon markets and keep things fair.

Flash swaps are performed when a certain level of dynamic minimum profit is obtained and then 98% of the profits are distributed to liquidity providers staking their token in the Farm section while 2% is kept by the protocol for further expansion, infrastructure maintenance, contests reward and much more.

---
description: FlashLiquidity Flash Swaps Farms overview
---

# Flash Swaps Farms

{% hint style="info" %}
**FlashLiquidity CREDITS:** Flash Swaps Farms implement a credits based system to distribute automated arbitrage profits.
{% endhint %}

Every Flash Swaps Farms distribute credits at a fixed rate of **8,64** **Credit/day** to liquidity providers staking their LP tokens.

Credits are emitted every second and distributed propotionally to the LP tokens staked by the user vs total amount of LP tokens staked in the contracts.

{% hint style="warning" %}
FlashLiquidity CREDITS are **not** ERC20 tokens, they have no direct value and cannot be transferred.
{% endhint %}

Credits are used exclusively as proof of user's staking time duration and to determine the user's entitled share of profits. &#x20;

When claiming profits from the farm contract the credits accumulated by the user are revoked and the proportional share of arbitrage profits is sent to the user address from the farm contract balance.&#x20;

Every farm contract distribute profits in one of the two token composing the corresponding pair (e.g. the reward token for the MATIC/ETH staking contract is MATIC)&#x20;

98% of the profits derived from automated arbitrage are distributed proportionally to liquidity providers staking their LP tokens while 2% are kept by the protocol for gas fees repayment (FlashLiquidity pays for arbitrage transaction gas fees in advance) , infrastructure maintenance, contests rewards and further expansion.

---
description: FlashLiquidity Flash Swaps Farms overview
---

# Flash Swaps Farms



{% hint style="info" %}
**CREDITS:** Staking contracts of Flash Swaps Farms  implement a credits based system for flash swaps profits distribution.
{% endhint %}

Every staking contracts of Flash Swaps Farms distribute credits at a fixed rate of **8,64** **Credit/day**.

Credits are emitted every second at a fixed rate and distributed propotionally to the LP tokens staked by the user vs the total amount of LP tokens staked in the contracts.

**Credits are not ERC20 tokens, they have no direct value and cannot be transferred.**

Credits are used exclusively as proof of user's staking time duration and determine the user's proportional share of profits. &#x20;

When claiming profits from the staking contract the credits accumulated by the user are revoked and the proportional share of profits is sent to the user address from the Staking contract balance.&#x20;

{% hint style="info" %}
Every Staking contract distribute profits in one of the two token composing the corresponding pair (for example reward token for the MATIC/ETH staking contract is MATIC)&#x20;
{% endhint %}

---
description: FlashLiquidity protocol overview
---

# Protocol overview

FlashLiquidity protocol is based upon [uniswap-v2](https://github.com/Uniswap/v2-core) pools and charges a flat fee of 0.30% for token swap:

* 0.25% is distributed proportionally to liquidity providers.
* 0.05% is used to buy back and partially burn [FLIQ](../fliq-token.md) tokens through the Incentivizer contract (derived from sushiswap [sushimaker](https://github.com/sushiswap/sushiswap/blob/canary/contracts/SushiMaker.sol) contract).

{% hint style="info" %}
Incentivizer contract burn all FLIQ tokens collected from FLIQ pairs fees while other tokens collected are converted and used to buy back FLIQ tokens.
{% endhint %}

FLIQ tokens bought back with the Incentivizer contract are then distributed to Flashliquidity FLIQ/MATIC liquidity providers staking their FLIQ/MATIC LP tokens in the Flash Swaps Farm section.

When prices diverge (between FlashLiquidity and other decentralized exchanges running on Polygon Network) FlashBot contracts perform arbitrages through Flash Swaps to equalize prices and make profits.

98% of the profits derived from flash swaps are distributed to liquidity providers staking their LP tokens in the Flash Swaps Farms section of the FlashLiquidity Interface.

Profits are distributed in one of the two token composing the FlashLiquidity pair in question.&#x20;

{% hint style="info" %}
example**:** MATIC-DAI pair distribute flashswaps profits in DAI.&#x20;
{% endhint %}

2% of the profits derived from Flash Swaps are kept by the protocol for gas fees repayment (FlashLiquidity pays for flash swaps gas fees in advance) , infrastructure maintenance, contests rewards and further expansion. &#x20;

{% hint style="info" %}
Currently Incentivizer is owned by FlashLiquidity developer.

Ownership will be transferred to a Governance contract when community will be ready and FLIQ tokens enough distributed.&#x20;
{% endhint %}
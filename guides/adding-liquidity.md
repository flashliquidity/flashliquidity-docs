---
description: Liquidity provision simplified
---

# Adding Liquidity

{% hint style="info" %}
**DYOR:** Impermanent loss (credits: Finematics):

[https://www.youtube.com/watch?v=8XJ1MSTEuU0](https://www.youtube.com/watch?v=8XJ1MSTEuU0)
{% endhint %}

## Liquidity provision

To add liquidity in one of the FlashLiquidity pools or even create a new pool you need first to possess some tokens in your Metamask wallet connected to Polygon blockchain.

Centralized Exchanges like Binance and Crypto.com offer direct Matic tokens withdrawal to the Polygon Pos chain with low fees.

Alternatively you could use [Quickswap](https://quickswap.exchange) fiat-on-ramp options to buy Matic tokens (directly on Polygon chain) with SEPA deposits or credit card.

Once you have some Matic tokens in your Metamask wallet connected to the Polygon chain you can swap thoose tokens to other assets of your choice in one of the many AMMs running on Polygon (Quickswap,Sushiswap,Apeswap,DFYN).

After thoose steps you should now possess the desired tokens to provide liquidity in one of the FlashLiquidity pools or even create a new one.

{% hint style="info" %}
Please note that only pairs composed by 18 decimals token support automated flash swaps and the new pair must have at least one external matching pair in other Polygon AMMs, new pairs that will not meet these requirements will be left open for public trading
{% endhint %}

Upon new pair creation, if above conditions are meet, a new FlashBot contract and a new Staking contract will be deployed and used to distribute Flash Swaps profits to liquidity providers staking their LP tokens in the Farm section of FlashLiquidity Interface.&#x20;



&#x20;  &#x20;

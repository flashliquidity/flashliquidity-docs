---
description: ⚡FlashLiquidity Documentation
---

# FlashLiquidity

{% hint style="warning" %}
This documentation is still under redaction.
{% endhint %}

### Brief introduction:

**FlashLiquidity**'s suite of DeFi products not only offers a diverse range of financial services but also **prioritizes transparency** and inclusivity in its operations.&#x20;

By providing transparent and immutable solutions for decentralized trading, automated arbitrage, yield generation, lending, and derivatives, FlashLiquidity aims to create a more accessible and inclusive financial landscape for everyone.&#x20;

**Decentralized Exchange**

FlashLiquidity's decentralized exchange stands out from other mainstream DEXs due to the unparalleled flexibility it offers with its trading pools.&#x20;

Unlike other DEXs, FlashLiquidity's pools can either be left open for public trading or managed by the self-balancing automation system, which distributes arbitrage profits to liquidity providers.&#x20;

1\) [Open pools](ecosystem/open-pools.md):&#x20;

* **open** for public trading.
* no front-running protection.
* standard 0.30% token swap fees to incentivize liquidity provision.

2\) [Self-balancing pools](ecosystem/self-balancing-pools.md):&#x20;

* trading is **not open** to the public.
* 0.06% token swap fees.
* The profits earned from arbitrage operations conducted by the self-balancing mechanism are distributed to liquidity providers via [liquid farming](ecosystem/liquid-farming/) instead of leaving them to external arbitrageurs.
*   FlashLiquidity's on-chain arbitrage automation leverages [Chainlink Automation](https://automation.chain.link) and [Chainlink Price Feeds ](https://data.chain.link/)to detect and perform profitable arbitrage operations between FlashLiquidity and other DEXs ensuring that price discrepancies are accurately detected, and arbitrage opportunities are swiftly executed.

    Unlike solutions on traditional centralized automation stacks, FlashLiquidity's arbitrage automation is fully decentralized, transparent, and resistant to manipulation.

**Liquid Farming** (fair distribution of arbitrage profits and FLIQ tokens):

In traditional yield farming systems, users deposit eligible tokens in a pool with other users in order to seek investment gains, typically through interest earned from lending the pooled tokens. These tokens accepted for deposit in the yield farm are commonly known as staking tokens.

In contrast, liquid farming operates by minting an equivalent amount of liquid farming tokens upon deposit of eligible LP tokens.&#x20;

For instance, when **ETH/USDC LP** tokens are deposited in the ETH/USDC farm, an equivalent amount of **fl-ETH/USDC** liquid token is minted, which is entitled to redeem the LP tokens deposited and the accrued rewards.

Liquid farming's true advantage lies in the **composability** of the yield strategies it enables. Liquid farming tokens can be used as collateral on centralized or decentralized markets or lending pools while still earning arbitrage profits on top of it.&#x20;

FlashLiquidity offers two different types of liquid farming:

1. **Arbitrage Farms**: distribute profits derived from self-balancing pools automation to liquidity providers staking their LP tokens in the farms, mint **stFLASH** liquid tokens upon LP tokens deposit.
2. **FLIQ Farms**: distribute FLIQ tokens allocated to FLIQ mining program to liquidity providers staking their LP tokens in the farms (coming soon).

**Lending** (coming soon)

FlashLiquidity's upcoming lending service will allow to use liquid farming tokens as collateral for loans providing users with more flexibility and opportunities to access capital, while also earning yield on their assets.&#x20;

This feature offers several advantages for users, including the ability to earn arbitrage profits on top of their collateral while still being able to access the capital they need.&#x20;

Additionally, because liquid farming tokens are designed to be composable with other DeFi protocols, they can be used to unlock additional yield opportunities, providing even more benefits for users.

### Guides: Jump right in

{% content-ref url="guides/add-liquidity-quickstart.md" %}
[add-liquidity-quickstart.md](guides/add-liquidity-quickstart.md)
{% endcontent-ref %}

{% content-ref url="guides/farming-quickstart.md" %}
[farming-quickstart.md](guides/farming-quickstart.md)
{% endcontent-ref %}

{% content-ref url="guides/how-to-claim-withdraw.md" %}
[how-to-claim-withdraw.md](guides/how-to-claim-withdraw.md)
{% endcontent-ref %}

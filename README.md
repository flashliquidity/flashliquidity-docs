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

Unlike other DEXs, FlashLiquidity's pools can either be left open for public trading or managed by the rebalancing automation, which distributes arbitrage profits to liquidity providers.&#x20;

1\) [Open pools](ecosystem/open-pools.md):&#x20;

* **open** for public trading.
* no front-running protection.
* standard 0.30% token swap fees to incentivize liquidity provision.

2\) [Self-balancing pools](ecosystem/self-balancing-pools.md):&#x20;

* trading is **not open** to the public.
* 0.06% token swap fees.
* These pools utilize Chainlink Data Streams (or Price Feeds) and  Chainlink Automation to monitor if the asset value ratios within the pool are unbalanced. If an imbalance is detected, the system calculates the size and direction of the required rebalancing trade. It then selects the most advantageous external decentralized exchange (DEX) to execute the arbitrage operation, aiming to maximize profits.
* The profits from these operations are periodically auto-compounded by adding liquidity back to the self-balancing pools to increase profitability and efficiency; the newly minted LP tokens are then distributed to liquidity providers.

### Guides: Jump right in

{% content-ref url="guides/add-liquidity-quickstart.md" %}
[add-liquidity-quickstart.md](guides/add-liquidity-quickstart.md)
{% endcontent-ref %}

{% content-ref url="guides/sbp-vaults-quickstart.md" %}
[sbp-vaults-quickstart.md](guides/sbp-vaults-quickstart.md)
{% endcontent-ref %}

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

---
description: ⚡FlashLiquidity Documentation
---

# FlashLiquidity

{% hint style="warning" %}
This documentation is still under redaction.
{% endhint %}

### Brief introduction:

FlashLiquidity is a rapidly expanding suite of DeFi products ranging from decentralized trading, automated arbitrage, yield generation, lending and derivatives.

**FlashLiquidity Decentralized Exchange** (Live on Polygon)

The key difference between FlashLiquidity decentralized exchange and other mainstream DEXs is that pools can be left open for public trading or managed by the self-balancing automation:

1\) [Open pools](ecosystem/open-pools.md):&#x20;

* **open** for public trading.
* no front-running protection.
* standard 0.30% token swap fees to incentivize liquidity provision.

2\) [Self-balancing pools](ecosystem/self-balancing-pools.md):&#x20;

* trading is **not open** to the public.
* 0.06% token swap fees.
* distribute profits derived from arbitrage operations done by the self-balancing mechanism to liquidity providers through [liquid farming](ecosystem/liquid-farming/).
* aritrage operations are ensured leveraging [Chainlink Automation](https://automation.chain.link) and [Chainlink Price Feeds ](https://data.chain.link/)without the risks associated with a centralized automation stack.

**Liquid Farming**:

In a traditional yield farming system, users can deposit elegible tokens in a pool with other users to seek investment gains, often through interest gained by lending the pooled tokens. (tokens accepted for deposit in the yield farm is often referred as the staking tokens)

With liquid farming an equivalent amount of [liquid farming token](ecosystem/liquid-farming/liquid-farming-tokens.md) is minted upon deposit of the elegible LP tokens.

Example: when depositing ETH/DAI LP tokens in the ETH/DAI farm an equivalent amount of fl-ETH/DAI liquid token is minted (entitled to redeem anytime the LP tokens deposited plus accrued rewards)&#x20;

Liquid farming's true advantage is the "composability" of the yield strategies it makes possible. Liquid farming tokens could be used as collateral on centralized or decentralized markets or lending pools while still earning arbitrage profits on top of it.

Two different type of liquid farming:

1\) [Arbitrage Farms](ecosystem/liquid-farming/arbitrage-farms.md): distribution of profits derived from self-balancing pools automation to liquidity providers staking their LP tokens in the farms. (**stFLASH** liquid tokens)

2\) [FLIQ Farms](ecosystem/liquid-farming/fliq-farms.md): distribution of FLIQ tokens allocated to FLIQ mining program to liquidity providers staking their LP tokens in the farms. (**stFLASHx** liquid tokens, coming soon)

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

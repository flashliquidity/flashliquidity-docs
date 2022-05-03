---
description: ⚡FlashLiquidity Documentation
---

# FlashLiquidity

![](.gitbook/assets/png\_20220415\_172744\_0000\(2\).png)

{% hint style="warning" %}
This documentation is still under redaction.
{% endhint %}

### Brief introduction:

FlashLiquidity is a decentralized protocol introducing self-balancing liquidity pools where both token swap fees and automated arbitrage revenues are distributed to liquidity providers.

FlashLiquidity is primarily a decentralized exchange running on Polygon mainnet and derived from [uniswap-v2](https://github.com/Uniswap/v2-core) with liquidity providers sharing a 0.25% fee of the trading volume as incentive.

{% hint style="success" %}
The **key difference** between **FlashLiquidity** and **Uniswap** is that pairs [can](./#requirements)\* be assigned to a privileged address (FlashSwapper smart contract) or left open for public trading. In the first case token swaps can only be performed by the **authorized address** hence blocking external arbitrageurs that could compete ([frontrunning](https://arxiv.org/pdf/2102.03347.pdf)) with automated flash swaps executed by the FlashSwapper contract making possible to distribute arbitrage profits to liquidity providers instead.&#x20;
{% endhint %}

FlashSwapper contracts performs [Flash Swaps](https://docs.uniswap.org/protocol/V2/guides/smart-contract-integration/using-flash-swaps) only when the deviation between the rates of the assigned FlashLiquidity pool and an equivalent external pool on another decentralized exchanges exceeds a minimum profit threshold.

Automated flash swaps rebalance FlashLiquidity pools back to fair markets prices for profits which are then distributed to liquidity providers staking their [LP tokens](https://coinmarketcap.com/alexandria/glossary/liquidity-provider-tokens-lp-tokens) in the [Flash Swaps Farm](https://www.flashliquidity.finance/#/farm/flashswap) section.

{% hint style="info" %}
Flash swaps profits are denominated in one of the two tokens composing the pair in question (example: ETH-DAI distribute arbitrage profits in ETH).
{% endhint %}

Alternatively liquidity providers can stake their LP tokens in the [FLIQ Farms ](ecosystem/farms/fliq-farms.md)section to receive [FLIQ](ecosystem/fliq-token.md) tokens at a fixed rate per second proportionally to their share of liquidity staked vs total liquidity staked in the pair in question (FLIQ Farms will be launched in the near future at the time of writing only Flash Swaps Farms are available).&#x20;

To get started just add liquidity to one of the pools of your choice and stake your LP tokens to receive a share of both token swap fees, flash swaps profits and/or FLIQ tokens.

#### Flash swaps requirements: <a href="#requirements" id="requirements"></a>

{% hint style="warning" %}
(**\***) Currently only pairs composed by 18 decimals token support automated flash swaps (new pair that will not meet this requirement will remain open for public trading but can still be included in the FLIQ liquidity mining program).
{% endhint %}

### Fundamentals

Learn the fundamentals of FlashLiquidity:

{% content-ref url="ecosystem/protocol-overview.md" %}
[protocol-overview.md](ecosystem/protocol-overview.md)
{% endcontent-ref %}

{% content-ref url="ecosystem/roadmap.md" %}
[roadmap.md](ecosystem/roadmap.md)
{% endcontent-ref %}

{% content-ref url="ecosystem/fliq-token.md" %}
[fliq-token.md](ecosystem/fliq-token.md)
{% endcontent-ref %}

{% content-ref url="ecosystem/farms/" %}
[farms](ecosystem/farms/)
{% endcontent-ref %}

### Guides: Jump right in

Follow our handy guides to get started on the basics as quickly as possible:

{% content-ref url="guides/add-liquidity-quickstart.md" %}
[add-liquidity-quickstart.md](guides/add-liquidity-quickstart.md)
{% endcontent-ref %}

{% content-ref url="guides/farming-quickstart.md" %}
[farming-quickstart.md](guides/farming-quickstart.md)
{% endcontent-ref %}

{% content-ref url="guides/how-to-claim-withdraw.md" %}
[how-to-claim-withdraw.md](guides/how-to-claim-withdraw.md)
{% endcontent-ref %}

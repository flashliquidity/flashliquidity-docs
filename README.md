---
description: >-
  ⚡FlashLiquidity is a Polygon Network protocol introducing self-balancing
  liquidity pools where automated arbitrage revenues are distributed to
  liquidity providers.
---

# FlashLiquidity

{% hint style="info" %}
This documentation is currently under redaction and incomplete.
{% endhint %}

{% hint style="info" %}
**AMM and Liquidity Pools terminology** are heavily used **** in the following paragraphs make sure to have a basic understanding of the subjects before diving further in this docs.

UniswapV2 docs:

[https://docs.uniswap.org/protocol/V2/introduction](https://docs.uniswap.org/protocol/V2/introduction)
{% endhint %}

### Brief introduction:

FlashLiquidity is built upon the [uniswap-v2](https://github.com/Uniswap/v2-core) liquidity pools technology with liquidity providers sharing 0.25% trading volume fee as incentive.

Every**\*** liquidity pool is paired one-on-one with a verified, non-upgradable smart contract called 'FlashBot' which is the only address authorized to swap tokens.

FlashBot contracts performs [Flash Swaps](https://docs.uniswap.org/protocol/V2/guides/smart-contract-integration/using-flash-swaps) when prices diverge between the assigned FlashLiquidity pool and others decentralized exchanges running on Polygon network (Quickswap, Sushiswap and many others).

Flash swaps equalize FlashLiquidity prices back to fair markets prices for profits which are then distributed to liquidity providers staking their [LP tokens](https://coinmarketcap.com/alexandria/glossary/liquidity-provider-tokens-lp-tokens) in the [Flash Swaps Farm](https://www.flashliquidity.finance/#/farm/flashswap) section of the [FlashLiquidity Interface](https://www.flashliquidity.finance/#/farm/flashswap)[.](https://www.flashliquidity.finance)

Alternatively liquidity providers can stake their LP tokens in the [FLIQ Farms ](fundamentals/farms/fliq-farms.md)section to receive [FLIQ](fundamentals/fliq-token.md) tokens at a fixed rate per second (proportionally to their share of liquidity staked vs total liquidity staked).&#x20;

To get started just add liquidity to one of the pools of your choice and stake your LP tokens to receive a share of both token swap fees, flash swaps profits and/or FLIQ tokens.

{% hint style="info" %}
(**\***) Currently only pairs composed by 18 decimals token support automated flashswaps (new pair that will not meet this requirement will remain open for public trading but can still be included in the FLIQ liquidity mining program).
{% endhint %}

### Fundamentals

Learn the fundamentals of FlashLiquidity:

{% content-ref url="fundamentals/protocol-overview/" %}
[protocol-overview](fundamentals/protocol-overview/)
{% endcontent-ref %}

{% content-ref url="fundamentals/roadmap.md" %}
[roadmap.md](fundamentals/roadmap.md)
{% endcontent-ref %}

{% content-ref url="fundamentals/fliq-token.md" %}
[fliq-token.md](fundamentals/fliq-token.md)
{% endcontent-ref %}

{% content-ref url="fundamentals/farms/" %}
[farms](fundamentals/farms/)
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

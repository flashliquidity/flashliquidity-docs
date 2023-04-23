# Self-balancing pools

{% hint style="success" %}
Arbitrage automation V2 is no longer limited to pairs composed by 18 decimals and compatible with Uniswap V2/V3 forks, Algebra (Quickswap V3) and Kyberswap elastic.
{% endhint %}

The **Arbiter** smart contract manages the self-balancing pools and continually scans prices across multiple decentralized exchanges to identify arbitrage opportunities.

Smart contracts are typically dormant and need an external entity to activate them and initiate a specific function. This can create a single point of failure where developers establish internal infrastructure to execute the function when required, leading to an unreliable and opaque solution.

By leveraging Chainlink Automation and Price Feeds FlashLiquidity has developed a fully automated system that searches for profitable on-chain arbitrage opportunities, executes the swap, and distributes the resulting gains to liquidity providers - all on-chain.&#x20;

This approach eliminates the need for a centralized automation stack, reducing associated risks and increasing transparency.



<figure><img src="../.gitbook/assets/Copia di FlashLiquidity(2).png" alt=""><figcaption><p>Integration with Chainlink Automation and Price Feeds</p></figcaption></figure>

The **Arbiter** contract utilizes Chainlink Automation to initiate arbitrage operations when the price difference between the assigned FlashLiquidity pool and an equivalent external pool on another decentralized exchange exceeds a minimum profit threshold. This minimum profit threshold is determined by using Chainlink Price Feeds.

Front running protection mechanism stop external arbitrageurs from competing with arbitrage operations.

Once executed, the automated arbitrage operations rebalance the FlashLiquidity pools back to fair market prices, generating profits that are then distributed to liquidity providers through the liquid farming mechanism.

# Self-balancing pools

{% hint style="success" %}
Arbitrage automation V2 is no longer limited to pairs composed by 18 decimals and compatible with Uniswap V2/V3 forks, Algebra (Quickswap V3) and Kyberswap elastic.
{% endhint %}

Self-balancing pools are managed by the **Arbiter** smart contract which constantly monitors prices across various decentralized exchanges on Polygon seeking arbitrage opportunities.

Smart contracts are natively asleep, and require an external entity to “wake” them up and trigger a particular function. This often introduces a single point of failure, in which developers set up in-house infrastructure that triggers the function when necessary — an inherently unreliable and opaque solution.



<figure><img src="../.gitbook/assets/Copia di FlashLiquidity(2).png" alt=""><figcaption><p>Integration with Chainlink Automation and Price Feeds</p></figcaption></figure>

By leveraging Chainlink Automation and Price Feeds it has been possible to build an end-to-end automated system for finding profitable on-chain arbitrage opportunities, carrying out the swap, and returning gains to liquidity providers entirely on-chain without the risks associated with a centralized automation stack.

<figure><img src="../.gitbook/assets/banner_flashliquidity_chainlink.jpg" alt=""><figcaption></figcaption></figure>

Chainlink Automation trigger arbitrage operation from the Arbiter contract when the deviation between the rates of the assigned FlashLiquidity pool and an equivalent external pool on another decentralized exchanges exceeds a minimum profit threshold (example: FlashLiquidity ETH-DAI pool and Quickswap ETH-DAI pool).

The minimum profit threshold is determined using Chainlink Price Feeds.

Front running protection mechanism stop external arbitrageurs from competing with arbitrage bots.

Automated artibrage operations rebalance FlashLiquidity pools back to fair markets prices for a profit that is then distributed to liquidity provider via liquid farming.

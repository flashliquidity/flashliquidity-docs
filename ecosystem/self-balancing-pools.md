# Self-balancing pools

The [Arbiter](https://github.com/flashliquidity/flashliquidity-arbiter) smart contract manages the self-balancing pools and continually **monitors** if the asset value ratios within the pool are unbalanced.&#x20;

If an imbalance is detected, the system calculates the size and direction of the required rebalancing trade and then selects the best external decentralized exchange as a counterparty to execute the arbitrage operation, aiming to maximize profits.&#x20;

Given the highly volatile nature of crypto assets, these strategic arbitrage operations can generate substantial profits, which are usually captured by external arbitrageurs in traditional DEX pools.&#x20;

The profits from these operations are periodically auto-compounded by adding liquidity back to the self-balancing pools to increase profitability and efficiency; the newly minted LP tokens are then distributed to liquidity providers.&#x20;

Smart contracts are typically dormant and need an external entity to activate them and initiate a specific function. This can create a single point of failure where developers establish internal infrastructure to execute the function when required, leading to an unreliable and opaque solution.&#x20;

By leveraging Chainlink Automation, FlashLiquidity has developed a fully automated system that searches for profitable on-chain arbitrage opportunities, executes the swap, and distributes profits to liquidity providers—all on-chain. This approach eliminates the need for a centralized automation stack, reducing associated risks and increasing transparency.&#x20;

The Arbiter **performs** rebalancing when the value ratio difference between the assigned FlashLiquidity pool and an equivalent external pool on another decentralized exchange exceeds a minimum arbitrage profit threshold. Once executed, the rebalancing operation brings the FlashLiquidity pools back to fair market prices.

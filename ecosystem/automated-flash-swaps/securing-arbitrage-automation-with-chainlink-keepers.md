# Securing Arbitrage Automation With Chainlink Keepers

[Chainlink Keepers](https://keepers.chain.link/) constantly monitor rates between FlashLiquidity pools and external pools on other decentralized exchanges to seek arbitrage opportunities.

Chainlink Keepers trigger flash swaps from FlashSwapper contract when the deviation between the rates of the assigned FlashLiquidity pool and an equivalent external pool on another decentralized exchanges exceeds a minimum profit threshold (example: FlashLiquidity ETH-DAI pool and Quickswap ETH-DAI pool).

The minimum profit threshold is determined using Chainlink Price Feeds.

Automated flash swaps rebalance FlashLiquidity pools back to fair markets prices for a profit that is then distributed to liquidity provider.

![](../../.gitbook/assets/finale\_keepers.png)

Chainlink Keepers is a leading solution to the problem of smart contract automation. Smart contracts are natively asleep, and require an external entity to “wake” them up and trigger a particular function. This often introduces a single point of failure, in which developers set up in-house infrastructure that triggers the function when necessary — an inherently unreliable and opaque solution.

To solve this problem, Chainlink Keepers leverage a decentralized and transparent pool of Keeper nodes to help provide strong guarantees around secure contract automation, saving teams time and mitigating the risks around manual interventions or centralized servers.

Chainlink Keepers are run by the same professional DevOps teams that have an established on-chain performance history of providing high reliability to Chainlink Price Feeds during extreme network congestion and market volatility.

Chainlink Keepers also have several gas-optimizing features that lower the costs of automating maintenance tasks for users, including a rotating node selection process to prevent gas price auction wars.

For the above reasons, Chainlink Keepers was the obvious choice to substitute the initial centralized off-chain infrastructure previously maintained by the FlashLiquidity team.

# Determining Profit Thresholds With Chainlink Price Feeds

By combining Chainlink Keepers and Price Feeds, FlashLiquidity has built an end-to-end automated system for identifying profitable arbitrage opportunities on-chain and triggering a transaction to make the swap and distribute profits back to LP providers entirely on-chain.

![](../../.gitbook/assets/farms\_final.png)

Chainlink Price Feeds has been the obvious choice to determine the profit threshold for arbitrage opportunities because they offer a multitude of superior features, such as:

* **High-Quality Data** — Chainlink Price Feeds source data from numerous premium data aggregators, leading to price data that’s aggregated from hundreds of exchanges, weighted by volume, and cleaned from outliers and suspicious volumes. Chainlink’s data aggregation model generates more precise global market prices that are resistant to API downtime, flash crash outliers, and data manipulation attacks like flash loans.
* **Secure Node Operators** — Chainlink Price Feeds are secured by independent, Sybil-resistant oracle nodes run by leading blockchain DevOps teams, data providers, and traditional enterprises with a strong track record for reliability, even during high gas prices and extreme network congestion.
* **Decentralized Network** — Chainlink Price Feeds are decentralized at the data source, oracle node, and oracle network levels, generating strong protections against downtime and tampering by the data provider or the oracle network.
* **Transparency** — Chainlink provides a robust reputation framework and set of on-chain monitoring tools that allow users to independently verify the historical performance of node operators and oracle networks, as well as check the real-time prices being offered.

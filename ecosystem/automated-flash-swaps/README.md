---
description: this page is currently under redaction and intentionally left empty
---

# Automated flash swaps

When a liquidity pair is assigned to a privileged address where a ‘FlashSwapper’ contract is deployed to handle the flash swaps execution logic and distribute arbitrage profits to liquidity providers. In the cases where a FlashSwapper contract is deployed, flash swaps can only be performed by the authorized FlashSwapper address  — blocking external arbitrageurs that could compete (through [frontrunning](https://arxiv.org/pdf/2102.03347.pdf)) with automated flash swaps executed by the FlashSwapper contract. This effectively makes it possible to distribute all arbitrage profits to liquidity providers instead of independent arbitrageurs.

To help automate and decentralize this process, we needed access to two different forms of oracle services — decentralized price data and secure smart contract automation.

![](../../.gitbook/assets/banner\_flashliquidity\_chainlink.jpg)

On April 14th 2022, FlashLiquidity protocol finished integrating [Chainlink Keepers](http://keepers.chain.link) and [Chainlink Data Feeds](http://data.chain.link) on Polygon mainnet. By integrating the industry-leading decentralized oracle network into the FlashLiquidity protocol, we now have access to decentralized price data and robust automation bots that help replace the centralized off-chain infrastructure handling pool rebalancing automation and arbitrage profit distributions to liquidity providers.

By doing so, we were able to eliminate a single point of failure and dramatically improve uptime, resiliency, and transparency.

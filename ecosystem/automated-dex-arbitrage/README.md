---
description: Automated flash swaps overview
---

# Automated DEX Arbitrage

FlashLiquidity protocol’s key differentiator is that liquidity providers can earn both a 0.25% fee of the trading volume as well as the arbitrage profits associated with keeping a liquidity pool balanced.

In order to distribute automated arbitrage profits to liquidity providers,without external arbitrageurs interfering in the process, liquidity pools can be assigned to a ‘FlashSwapper’ contract that handle flash swaps execution logic.&#x20;

When a pool is assigned to a FlashBot contract, flash swaps can only be performed by the authorized FlashBot address  — blocking external arbitrageurs that could compete (through [frontrunning](https://arxiv.org/pdf/2102.03347.pdf)) with automated flash swaps executed by the FlashBot contract. This effectively makes it possible to distribute all arbitrage profits to liquidity providers instead of independent arbitrageurs.

To help automate and decentralize this process, we needed access to two different forms of oracle services — decentralized price data and secure smart contract automation.

![](../../.gitbook/assets/banner\_flashliquidity\_chainlink.jpg)

On April 14th 2022, FlashLiquidity protocol finished integrating [Chainlink Keepers](http://keepers.chain.link) and [Chainlink Data Feeds](http://data.chain.link) on Polygon mainnet. By integrating the industry-leading decentralized oracle network into the FlashLiquidity protocol, we now have access to decentralized price data and robust automation bots that help replace the centralized off-chain infrastructure handling pool rebalancing automation and arbitrage profit distributions to liquidity providers.

By doing so, we were able to eliminate a single point of failure and dramatically improve uptime, resiliency, and transparency.

![](../../.gitbook/assets/integration\_overview.png)

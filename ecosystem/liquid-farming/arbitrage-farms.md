---
description: Self-balancing pools profits distribution
---

# Arbitrage farms

Profits from self-balancing automation are distributed to liquidity providers staking their LP tokens in the farm.

Everytime an arbitrage operation is carried out by the bot smart contracts of a self-balancing pool, the profits realized are immediately routed to the correspondent arbitrage farm to be shared proportionally by LP stakers.

LP stakers receives an equal amount of stFLASHa liquid tokens upon LP tokens deposit in the farm.

{% hint style="success" %}
Every farm contract distribute profits in one of the two token composing the corresponding pair (e.g. the rewards token for the ETH/DAI arbitrage farm is ETH)
{% endhint %}

<figure><img src="../../.gitbook/assets/Copia di FlashLiquidity(5).png" alt=""><figcaption><p>(ETH-DAI arbitrage farm distrbute profits in ETH and mint/burns fl-ETH/DAI (stFLASHa) liquid tokens</p></figcaption></figure>



Arbitrage farms implement a fixed-rate credits based system to distribute arbitrage profits.

Every arbitrage farm distribute credits at a fixed rate of **8,64** **Credit/day** to liquidity providers proportionally to their staked LP tokens amount. (Credits are emitted every seconds)

{% hint style="success" %}
Credits are **not** ERC20 tokens, they have no direct value but are entitled to redeem the proportional amount of rewards token from the arbitrage farm.

When sending stFLASHa liquid tokens between accounts also the credits accrued are moved proportionally to the receiver.
{% endhint %}

Credits are used exclusively as proof of user's staking time duration and to determine the user's entitled share of profits. &#x20;

When claiming profits from the farm contract the credits accumulated are revoked and the proportional share of arbitrage profits is sent to the user address from the farm contract balance. &#x20;

98% of the profits derived from automated arbitrage are distributed proportionally to liquidity providers staking their LP tokens while 2% are kept by the protocol for gas fees repayment (FlashLiquidity pays for arbitrage transaction gas fees in advance) , infrastructure maintenance, contests rewards and further expansion.

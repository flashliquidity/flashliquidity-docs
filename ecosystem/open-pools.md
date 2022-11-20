# Open pools

A pair of ERC20 tokens can be traded in each Flashliquidity pool.&#x20;

Because each token's balance in a pool contract is initially 0, someone must seed the pool with an initial deposit of each token before it can begin facilitating trades.

{% hint style="info" %}
The initial price of the pool is determined by this first liquidity provider.&#x20;
{% endhint %}

There is a motivation for liquidity providers to add both tokens with equal value to the pool. If the initial liquidity provider deposits tokens at a ratio differing from the current market rate, this would immediately create a profitable arbitrage opportunity that would likely be taken advantage of by a third party.

<figure><img src="../.gitbook/assets/Copia di FlashLiquidity(3).png" alt=""><figcaption><p>example ETH-DAI pool</p></figcaption></figure>

Unique tokens known as liquidity tokens are created and transferred to the provider's address whenever liquidity is deposited into a pool.&#x20;

These coins represent the contribution to a pool made by a certain liquidity provider. The number of liquidity tokens the provider receives is based on the percentage of the pool's liquidity that is delivered.&#x20;

{% hint style="info" %}
The quantity of liquidity tokens that the provider will receive if they are creating a new pool is equal to sqrt(x \* y), where x and y stand for the quantity of each token offered.
{% endhint %}

Every time a trade happens, the transaction sender is charged a 0.3% fee.&#x20;

Upon the completion of the trade, the fee is distributed proportionally to each liquidity providers in the pool (0.25% to liquidity providers, 0.05% is retained by the protocol to buy back and burn FLIQ tokens).&#x20;

# Glossary

#### Automated market maker <a href="#automated-market-maker" id="automated-market-maker"></a>

An automated market maker is a smart contract that holds on-chain liquidity reserves. Users can trade against these reserves at prices set by an automated market making formula.

#### Constant product formula <a href="#constant-product-formula" id="constant-product-formula"></a>

The automated market making algorithm used by FlashLiquidity. See [x\*y=k](automated-market-maker/).

#### ERC20 <a href="#erc20" id="erc20"></a>

ERC20 tokens are fungibile tokens on Ethereum and Polygon.

#### Factory <a href="#factory" id="factory"></a>

A smart contract that deploys a unique smart contract for any ERC20/ERC20 trading pair.

#### Pair <a href="#pair" id="pair"></a>

A smart contract that enables trading between two ERC20 tokens (FlashLiquidity pairs can be assigned exclusively to an address or left open for public trading).

#### Pool <a href="#pool" id="pool"></a>

Liquidity within a pair is pooled across all liquidity providers.

#### Liquidity provider / LP <a href="#liquidity-provider--lp" id="liquidity-provider--lp"></a>

A liquidity provider is someone who deposits an equivalent value of two ERC20 tokens into the liquidity pool within a pair. Liquidity providers take on price risk and are compensated with fees and a share of automated arbitrage revenues.

#### Flash swap <a href="#flash-swap" id="flash-swap"></a>

A trade that uses the tokens being purchased before paying for them.

#### `x * y = k` <a href="#x--y--k" id="x--y--k"></a>

The constant product formula.

#### Invariant <a href="#invariant" id="invariant"></a>

The "k" value in the constant product formula

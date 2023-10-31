# Minting Synthetic Assets (SuTokens)

### <mark style="background-color:blue;">Which SuTokens are currently supported</mark>&#x20;

At launch, SuETH, suUSD and suBTC will be supported

### <mark style="background-color:blue;">What are homogeneous and Heterogeneous groups that determine the mint limit for assets?</mark>&#x20;

Homogeneous Group – Assets that represent same underlying risk profile, liquidity and value&#x20;

* USD - USDC, USDT, DAI
* ETH - WETH, wstETH&#x20;
* BTC - WBTC, tBTC&#x20;

Heterogeneous Group – Assets that do not represent the same underlying value&#x20;

* USDC ≠ ETH ≠ BTC

### <mark style="background-color:blue;">**What is Mint Rate?**</mark>

Loan to Value available to mint SuTokens from deposited assets within the same homogeneous group (USDC to SuUSD)&#x20;

They have the maximum LTV available within the protocol

### <mark style="background-color:blue;">**What is Intra Collateral Rate?**</mark>

Loan to Value available to borrow native assets from either deposited native assets or deposited SuTokens within the same homogeneous group (USDC to USDT or SuUSD to USDT)&#x20;

They have the lower LTV than Intra SuLTV within the protocol

### <mark style="background-color:blue;">**What is Inter Collateral Rate?**</mark>

Loan to Value available to mint SuTokens or borrow native assets from deposited assets across a different heterogeneous group (USDC to SuETH or USDC to WBTC)&#x20;

They have the lowest LTV available within the protocol

### <mark style="background-color:blue;">How is mint limit determined when multiple assets are deposited as collateral</mark>&#x20;

Homogeneous assets are given priority over heterogeneous groups for determining the mint limit when multiple assets are deposited as collateral

### <mark style="background-color:blue;">What is the cost incurred to mint SuTokens</mark>&#x20;

At launch, there is no cost to mint SuTokens apart from the loss in any capital efficiency due to the LTV available. In the case of Homogeneous SuToken mints with LTV close to 1, there is a marginal loss in capital efficiency.&#x20;

The protocol has a design incorporated for SuToken exit fee and SuToken mint interest. Both the values are ‘0’ at launch

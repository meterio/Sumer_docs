# Minting Synthetic Assets (SuTokens)

### Which SuTokens are currently supported&#x20;

At launch, SuETH, suUSD and suBTC will be supported

### What are homogeneous and Heterogeneous groups that determine the mint limit for assets?&#x20;

Homogeneous Group – Assets that represent same underlying risk profile, liquidity and value&#x20;

* USD - USDC, USDT, BUSD
* ETH - ETH, BETH (BSC), WETH&#x20;
* BTC - WBTC, RenBTC&#x20;

Heterogeneous Group – Assets that do not represent the same underlying value&#x20;

* USDC ≠ ETH ≠ BTC

### **What is Intra SuLTV?**

Loan to Value available to mint SuTokens from deposited assets within the same homogeneous group (USDC to SuUSD)&#x20;

They have the maximum LTV available within the protocol

### **What is Intra LTV?**

Loan to Value available to borrow native assets from either deposited native assets or deposited SuTokens within the same homogeneous group (USDC to USDT or SuUSD to USDT)&#x20;

They have the lower LTV than Intra SuLTV within the protocol

### **What is Inter LTV?**

Loan to Value available to mint SuTokens or borrow native assets from deposited assets across a different heterogeneous group (USDC to SuETH or USDC to WBTC)&#x20;

They have the lowest LTV available within the protocol

### How is mint limit determined when multiple assets are deposited as collateral&#x20;

Homogeneous assets are given priority over heterogeneous groups for determining the mint limit when multiple assets are deposited as collateral

### What is the cost incurred to mint SuTokens&#x20;

At launch, there is no cost to mint SuTokens apart from the loss in any capital efficiency due to the LTV available. In the case of Intra SuLTV mints with LTV close to 1, there is a marginal loss in capital efficiency.&#x20;

The protocol has a design incorporated for SuToken exit fee and SuToken mint interest. Both the values are ‘0’ at launch

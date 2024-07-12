# Borrow Native Assets

Using the supplied assets or SuToken as collateral, users can borrow native assets (USDC, USDT, DAI, ETH, WBTC) from Sumer’s borrowing facility.&#x20;

### <mark style="background-color:blue;">Collateral Rate or LTV</mark>

Each borrow position carries Collateral Rates (i.e. Loan-to-Value ratio), which signify the amount available to be borrowed for each collateralized asset.&#x20;

A Collateral Rate of 75% means that the users can only borrow up to 75% of the value of their collateralized assets.&#x20;

Applicable Collateral Rates while borrowing from Sumer are;

#### <mark style="background-color:blue;">Intra Collateral Rate or LTV</mark>

The maximum value of asset that can be borrowed when collateral and borrowing asset belong to the same homogeneous group

<mark style="color:yellow;">For e.g. Borrowing ETH by supplying stETH</mark>

#### <mark style="background-color:blue;">Inter Collateral Rate or LTV</mark>

The maximum value of asset that can be borrowed when collateral and borrowing asset belong to the different heterogeneous group

<mark style="color:yellow;">For e.g. Borrowing ETH by supplying USDC or Minting suETH by supplying USDT</mark>&#x20;

### <mark style="background-color:blue;">Borrow Limit</mark>

The borrow limit is yielded as the sum of locked collateral value, times the maximum LTV ratio of collateral

Borrows can be made until the user's liability reaches their position's borrow limit. . One should observe that the borrowing limit fluctuates with the oracle-reported deposit asset price.&#x20;

### <mark style="background-color:blue;">Borrow Interest</mark>&#x20;

The protocol charges users' interest while repaying the borrowed assets.&#x20;

<mark style="color:yellow;">**Each borrowing will carry a compounded interest determined based on the interest rate model specific to the borrowed asset.**</mark>&#x20;

The loan can be repaid anytime by the user. Any changes to the interest rate model will be made through the governance process.&#x20;

### <mark style="background-color:blue;">Timelock</mark>

At launch, Sumer has Timelock introduced for withdrawal of borrowed assets.&#x20;

<mark style="color:yellow;">Users cannot withdraw borrowed assets within the same block in which the collateral is supplied.</mark>&#x20;

### <mark style="background-color:blue;">Protocol Parameters</mark>

Key Protocol Parameter determined through the Governance process are;&#x20;

1. Intra LTV (IntraCratemantissa)&#x20;
2. Inter LTV (InterCratemantissa)
3. Borrow Limit (User)
4. Interest Rate Model

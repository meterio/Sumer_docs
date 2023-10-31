# Collateral Factor by Asset Group

### <mark style="background-color:blue;">Collateral Factor by Asset Grouping</mark>&#x20;

<mark style="color:yellow;">Sumer determines the ability to borrow assets or mint SuTokens based on the group of asset (homogeneous and heterogeneous) supplied as collateral.</mark>

Borrow/ Mint within same asset group = Higher LTV similar risk profile

Borrow/ Mint across different asset group = Lower LTV due to varying risk profile

### <mark style="background-color:blue;">Collateral Factor or LTV</mark>

Collateral Factor (i.e. Loan-to-Value ratio) signifies the value available to be borrowed/ minted for each collateralized asset.&#x20;

A Collateral Factor of 75% means that the users can only borrow up to 75% of the value of their collateralized assets.&#x20;

<mark style="color:yellow;">The Collateral Factor for each asset is set based on several inherent characteristics of the asset, such as availability in the reserve, normalized volatility and the asset’s liquidity in the market.</mark>&#x20;

_<mark style="color:yellow;">**NOTE:**</mark>_ These ratios and their parameters will be determined by the Sumer Team at launch. As the protocol matures and the necessary framework is in place, the governance of these parameters will be opened to the community via Sumer’s governance process.

#### <mark style="background-color:blue;">Intra Collateral Rate or LTV</mark>

The maximum value of asset that can be borrowed when collateral and borrowing asset belong to the same homogeneous group

<mark style="color:yellow;">For e.g. Borrowing ETH by supplying stETH</mark>

#### <mark style="background-color:blue;">Mint Rate</mark>

The maximum value of SuToken that can be minted when collateral and SuToken asset belong to the same homogeneous group

By design, The Mint Rate has the highest LTV for supplied assets (close to 1)

<mark style="color:yellow;">For e.g. Minting  suETH by supplying ETH</mark>

#### <mark style="background-color:blue;">Inter Collateral Rate or LTV</mark>

The maximum value of asset that can be borrowed or minted when collateral and borrowing asset belong to the different heterogeneous group

<mark style="color:yellow;">For e.g. Borrowing ETH by supplying USDC or Minting suETH by supplying USDT</mark>&#x20;

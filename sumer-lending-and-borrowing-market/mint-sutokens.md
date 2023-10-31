---
description: Sumer Synthetic Assets
---

# Mint SuTokens

Using their supplied assets as collateral, users can mint SuTokens (Initially SuUSD, SuETH, SuBTC.) from Sumer’s mint function to be traded, farmed or spent across multiple chains.&#x20;

### <mark style="background-color:blue;">Collateral Factor or LTV</mark>

Each SuToken carries Collateral Factors (i.e. Loan-to-Value ratio), which signify the amount available to be minted for each collateralized asset.&#x20;

A Collateral Factor of 75% means that the users can only borrow up to 75% of the value of their collateralized assets.&#x20;

Applicable Collateral factors while minting SuTokens are;

#### <mark style="background-color:blue;">Mint Rate</mark>

The maximum value of SuToken that can be minted when collateral and SuToken asset belong to the same homogeneous group

By design, The Mint Rate has the highest LTV for supplied assets (close to 1)

<mark style="color:yellow;">For e.g. Minting  suETH by supplying ETH</mark>

#### <mark style="background-color:blue;">Inter Collateral Rate or LTV</mark>

The maximum value of asset that can be borrowed or minted when collateral and borrowing asset belong to the different heterogeneous group

<mark style="color:yellow;">For e.g. Borrowing ETH by supplying USDC or Minting suETH by supplying USDT</mark>&#x20;

### <mark style="background-color:blue;">Mint Limit</mark>

The Mint limit is yielded as the sum of locked collateral value, times the maximum LTV of collateral

Mints can be made until the user's liability reaches their position's Mint limit. One should observe that the Mint limit fluctuates with the oracle-reported deposit asset price.&#x20;

### <mark style="background-color:blue;">Mint Fee</mark>&#x20;

The protocol has the option to charge users' interest on minting while repaying the minted SuTokens.&#x20;

<mark style="color:yellow;">**The mint interest is set as 0% at the launch of the protocol.**</mark>&#x20;

Any changes to the mint interest will be made through the governance process.&#x20;

### <mark style="background-color:blue;">Timelock</mark>

At launch, Sumer has Timelock introduced for withdrawal of minted SuTokens.&#x20;

<mark style="color:yellow;">Users cannot withdraw minted SuTokens within the same block in which the collateral is supplied.</mark>&#x20;

### <mark style="background-color:blue;">Protocol Parameters</mark>

Key Protocol Parameter determined through the Governance process are;&#x20;

1. Intra SuLTV (Intramintratemantissa)
2. Inter LTV (InterCratemantissa)
3. Mint Limit (User)

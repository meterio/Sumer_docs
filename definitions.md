# Definitions

### <mark style="background-color:blue;">Collateral</mark>

In order to borrow native tokens or mint SuTokens from the Sumer protocol, users need to first supply another native asset or SuTokens as collateral.&#x20;

Supplied collateral assets earn interest while in the protocol, but users cannot redeem or transfer assets while they are being used as collateral against an open borrow.

### <mark style="background-color:blue;">Collateral Rate</mark>

The maximum amount users can borrow is limited by the collateral factors of the assets they have supplied.&#x20;

For example, if a user supplies 100 USDC as collateral, and the posted collateral factor for USDC is 90%, then the user can borrow at most 90 USDC worth of other native tokens at any given time. Each asset in Sumer Protocol can have a different collateral factor.&#x20;

#### <mark style="background-color:blue;">Intra Collateral Rate or IntraCratemantissa</mark>

The maximum value of homogeneous asset that can be borrowed with this asset as collateral&#x20;

(For e.g. Deposit ETH, borrow stETH)

#### <mark style="background-color:blue;">Inter Collateral Rate or InterCratemantissa</mark>

The maximum value of heterogeneous asset that can be borrowed with this asset as collateral&#x20;

(For e.g. Deposit ETH, borrow USDC or Deposit ETH, mint suUSD)

#### <mark style="background-color:blue;">Mint Rate or Intramintratemantissa</mark>

The maximum value of Homogeneous SuToken that can be minted with this asset as collateral&#x20;

(For e.g. Deposit ETH, mint suETH)

#### <mark style="background-color:blue;">Intrasuratemantissa</mark>

The maximum value of Homogeneous asset that can be borrowed with SuToken as collateral&#x20;

(For e.g. Deposit suETH, borrow ETH)

#### <mark style="background-color:blue;">Intersuratemantissa</mark>

The maximum value of Heterogeneous asset that can be borrowed with SuToken as collateral

(For e.g. Deposit suETH, borrow USDC or WBTC)

### <mark style="background-color:blue;">Loan to Value</mark>

The Loan to Value (LTV) ratio defines the maximum amount of currency that can be borrowed with specific collateral. It’s expressed in percentage: at LTV=75%, for every 1 ETH worth of collateral, borrowers will be able to borrow 0.75 ETH worth of the corresponding currency. Once a loan is taken, the LTV evolves with market conditions.&#x20;

### <mark style="background-color:blue;">Borrow Balance</mark>&#x20;

This is the sum of a user’s current borrowed amount plus the interest that needs to be repaid.&#x20;

### <mark style="background-color:blue;">Borrow Rate</mark>&#x20;

Borrowers owe the prevailing interest rate of the asset they are borrowing. This is done by adding the Borrow Rate to the account’s Borrow Balance for every block on the supported Network. While a borrow is open, the Borrow Balance is **ever-increasing**. The borrow and interest are never required to be repaid unless the borrower becomes insolvent; otherwise, the borrower can choose to repay some or all of their borrowing whenever they choose.

### <mark style="background-color:blue;">Reserve Factor or reserveFactorMantissa</mark>

The percentage of the spread between borrower's and lender's interest rates that accrue to the Sumer Protocol's treasury&#x20;

Example: Reserve factor of 20% means that 20% of the interest paid on the asset is for the protocol.

### <mark style="background-color:blue;">Close Factor or closeFactorMantissa</mark>&#x20;

The maximum amount that can be liquidated in a single transaction Example: 50% Close Factor means that a maximum of 50% of an account's borrow that is enabled as collateral can be repaid in a single liquidate transaction.

### <mark style="background-color:blue;">Liquidation Incentive</mark>

The additional collateral paid to the liquidators as an incentive to perform liquidation of underwater accounts. For example, if the liquidation incentive is 1.1, liquidators receive an extra 10% of the borrowers' collateral for every unit they close.

#### <mark style="background-color:blue;">heteroLiquidationIncentiveMantissa</mark>&#x20;

Liquidation Incentive when collateral supplied and assets borrowed are heterogeneous

#### <mark style="background-color:blue;">homoLiquidationIncentiveMantissa</mark>&#x20;

Liquidation Incentive when collateral supplied and assets borrowed are homogeneous

#### <mark style="background-color:blue;">sutokenLiquidationIncentiveMantissa</mark>&#x20;

Liquidation Incentive when collateral supplied and SuToken minted are homogeneous

### <mark style="background-color:blue;">Liquidation Threshold</mark>

The liquidation threshold is the percentage at which a loan is defined as undercollateralized. For example, a Liquidation threshold of 80% means that if the value rises above 80% of the collateral, the loan is undercollateralized and could be liquidated. The delta between the Loan-To-Value and the Liquidation Threshold is a safety cushion for borrowers.

### <mark style="background-color:blue;">Deposit Cap or maxSupply</mark>

For the security of the Sumer Protocol, Supply caps are used to limit the protocol’s exposure to riskier assets and protect against exploits (for e.g. infinite mints).

Every asset supplied as collateral for minting SuTokens or borrowing native assets will be subjected to a deposit cap based on the on-chain liquidity of the asset.

### <mark style="background-color:blue;">Borrow Cap or borrowCap</mark>

For the security of the Sumer Protocol, Borrow caps are used to prevent traditional and flash borrowing of an asset (for e.g. experiencing a price exploit) that can impact protocol solvency.

Every asset borrowed will be subjected to a borrow cap based on the on-chain liquidity of the asset.

### <mark style="background-color:blue;">Homogeneous Asset Group</mark>

Assets within this group consist of tokens with similar value, liquidity, and risk profile.

For e.g.: USDC, USDT, and BUSD will represent homogeneous assets within the same group. Alternative stable coins (e.g.: MIM or FRAX) would not be in the same asset group due to the difference in risk profile when compared to USDC, USDT and BUSD.

### <mark style="background-color:blue;">Heterogeneous Asset Group</mark>

Assets within this group consist of tokens with varying value, liquidity and risk profile.

For e.g.: USDC, ETH and BTC will represent heterogeneous assets.

### <mark style="background-color:blue;">Interest Rate Model - Base Rate or baseRatePerYear</mark>

It is the minimum (floor) borrowing rate of the liquidity pool

### <mark style="background-color:blue;">Interest Rate Model - Kink Point or kink</mark>&#x20;

It is the cut-off point in utilization rate where interest rate follows the Jump Model (e.g., 80%)&#x20;

### <mark style="background-color:blue;">Interest Rate Model - Jump Multiplier or jumpMultiplierPerYear</mark>

It is the Scale factor per utilization under the Jump Model


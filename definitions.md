# Definitions

* Collateral

In order to borrow native tokens or mint SuTokens from the Sumer protocol, users need to first supply another native asset or SuTokens as collateral. This is provided using the same **mint** function used for supplying assets. Supplied collateral assets earn interest while in the protocol, but users cannot redeem or transfer assets while they are being used as collateral against an open borrow.

* Collateral Factor

The maximum amount users can borrow is limited by the collateral factors of the assets they have supplied. For example, if a user supplies 100 USDC as collateral, and the posted collateral factor for USDC is 90%, then the user can borrow at most 90 USDC worth of other native tokens at any given time. Each asset in Sumer Protocol can have a different collateral factor.&#x20;

* Loan to Value

The Loan to Value (LTV) ratio defines the maximum amount of currency that can be borrowed with specific collateral. It’s expressed in percentage: at LTV=75%, for every 1 ETH worth of collateral, borrowers will be able to borrow 0.75 ETH worth of the corresponding currency. Once a loan is taken, the LTV evolves with market conditions.&#x20;

* Borrow Balance&#x20;

This is the sum of a user’s current borrowed amount plus the interest that needs to be repaid.&#x20;

* Borrow Rate&#x20;

Borrowers owe the prevailing interest rate of the asset they are borrowing. This is done by adding the Borrow Rate to the account’s Borrow Balance for every block on the supported Network. While a borrow is open, the Borrow Balance is **ever-increasing**. The borrow and interest are never required to be repaid unless the borrower becomes insolvent; otherwise, the borrower can choose to repay some or all of their borrowing whenever they choose.

* Reserve Factor&#x20;

The percentage of the spread between borrower's and lender's interest rates that accrue to the Sumer Protocol's treasury&#x20;

Example: Reserve factor of 20% means that 20% of the interest paid on the asset is for the protocol.

* Close Factor&#x20;

The maximum amount that can be liquidated in a single transaction Example: 50% Close Factor means that a maximum of 50% of an account's borrow that is enabled as collateral can be repaid in a single liquidate transaction.

* Liquidation Fee

The additional collateral paid to the liquidators as an incentive to perform liquidation of underwater accounts. For example, if the liquidation incentive is 1.1, liquidators receive an extra 10% of the borrowers' collateral for every unit they close.

* Liquidation Threshold&#x20;

The liquidation threshold is the percentage at which a loan is defined as undercollateralized. For example, a Liquidation threshold of 80% means that if the value rises above 80% of the collateral, the loan is undercollateralized and could be liquidated. The delta between the Loan-To-Value and the Liquidation Threshold is a safety cushion for borrowers.

* Deposit Cap

For the security of the Sumer Protocol, primarily against Flash Loan Attacks; every asset supplied as collateral for minting SuTokens or borrowing native assets will be subjected to a deposit cap based on the on-chain liquidity of the asset.

* Homogeneous Asset Group

Assets within this group consist of tokens with similar value, liquidity, and risk profile.

For e.g.: USDC, USDT, and BUSD will represent homogeneous assets within the same group. Alternative stable coins (e.g.: MIM or FRAX) would not be in the same asset group due to the difference in risk profile when compared to USDC, USDT and BUSD.

* Heterogeneous Asset Group

Assets within this group consist of tokens with varying value, liquidity and risk profile.

For e.g.: USDC, ETH and BTC will represent heterogeneous assets.

* Base Rate&#x20;

It is the minimum (floor) borrowing rate of the liquidity pool

* Kink Point&#x20;

It is the cut-off point in utilization rate where interest rate follows the Jump Model (e.g., 80%)&#x20;

* Jump Multiplier&#x20;

It is the Scale factor per utilization under the Jump Model&#x20;


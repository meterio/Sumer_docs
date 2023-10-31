# Repay Borrowed Native Assets

Users can repay the borrowed native assets to the Sumer Protocol up to the borrowed balance.&#x20;

### <mark style="background-color:blue;">Multiple Collateral Assets</mark>

By default, if multiple assets are supplied as collateral to get into a borrow position, the collateral available for withdrawal will be the asset with lower Loan to Value.&#x20;

### <mark style="background-color:blue;">Partial Repayment</mark>

Users can make partial repayment of their borrowing liability. On partial repayment, the borrow liability will be non-zero and will continue to accrue interest.

Also, not all collateral is available for withdrawal on partial repayment of borrowing.&#x20;

### <mark style="background-color:blue;">Borrow Interest</mark>

The protocol charges users' interest while repaying the borrowed assets.&#x20;

<mark style="color:yellow;">**Each borrowing will carry a compounded interest determined based on the interest rate model specific to the borrowed asset.**</mark>&#x20;

The loan can be repaid anytime by the user. Any changes to the interest rate model will be made through the governance process.&#x20;

### <mark style="background-color:blue;">Health Factor</mark>

The health factor represents the safety of your deposited assets against the borrowed assets and its underlying value. The higher the value is, the safer the state of your funds are against a liquidation scenario.&#x20;

If the health factor reaches 1, liquidation of your deposits will be triggered. A Health Factor below 1 can get liquidated.&#x20;

<mark style="color:yellow;">The health factor depends on the liquidation threshold of your collateral against the value of your borrowed funds.</mark>

# Borrowing Native Assets

1. Using the supplied assets or SuToken as collateral, users can borrow native assets (USDC, USDT, ETH, WBTC, BNB, BUSD) from Sumer’s borrowing facility.&#x20;
2. Each asset carries Collateral Factors (i.e., Loan-to-Value ratio), which signify the amount available to be borrowed for each collateralized asset. A Collateral Factor of 75% means that the users can only borrow up to 75% of the value of their collateralized assets.&#x20;
3. Borrows can be made until the user's liability reaches their position's borrow limit. The borrow limit is yielded as the sum of locked collateral value, times the maximum LTV ratio of collateral. One should observe that the borrow limit fluctuates with the oracle-reported deposit asset price.&#x20;
4. Each loan will carry a compounded interest rate and can be repaid at any time.&#x20;
5. The Collateral Factor for each asset is set based on several inherent characteristics of the asset, such as availability in the reserve and asset’s liquidity in the market. These ratios and their parameters will be determined by the Sumer Team, however as the protocol matures and the necessary processes are in place, the governance of these parameters will be opened to the community via Sumer’s governance process.&#x20;
6. Key Protocol Parameter determined through Governance process are;&#x20;
   1. Optimal Utilization Rate&#x20;
   2. Borrow Interest Rate&#x20;
   3. Borrow Limit (User)

# Minting Sumer Assets

1. Using their supplied assets as collateral, users can mint SuTokens (Initially SuUSD, SuETH, SuBTC.) from Sumer’s mint function to be traded, farmed or spent across multiple chains.&#x20;
2. Each SuToken carries Collateral Factors (i.e. Loan-to-Value ratio), which signify the amount available to be minted for each collateralized asset. A Collateral Factor of 75% means that the users can only borrow up to 75% of the value of their collateralized assets.&#x20;
3. **Sumer introduces a concept of homogeneous and heterogeneous asset group classification.** Each asset group consists of tokens with similar value, liquidity, and risk factor. For example USDC, USDT, BUSD, and suUSD are homogeneous assets and belong to the same asset group.&#x20;
4. When Sumer’s risk engine calculates the collateral values, it uses INTRA-LTV and INTRA-SuLTV for liabilities within the same homogeneous group and INTER-LTV for liabilities across different heterogeneous asset groups.&#x20;
5. Mints can be made until the user's liability reaches their position's Mint limit. The Mint limit is yielded as the sum of locked collateral value, times the maximum LTV ratio of collateral. One should observe that the Mint limit fluctuates with the oracle-reported deposit asset price.&#x20;
6. Users can lock multiple native assets types to a single position, diversifying collateral price exposure.&#x20;
7. The Collateral Factor for each asset is set based on several inherent characteristics of the asset, such as availability in the reserve and the asset’s liquidity in the market. These ratios and their parameters will be determined by the Sumer Team, however as the protocol matures and the necessary processes are in place, the governance of these parameters will be opened to the community via Sumer’s governance process.
8. The protocol has the option to charge users' interest on minting while repaying the minted SuTokens. However, **the minting interest is set as 0% at the launch of the protocol**. Any changes to the mint interest will be made through the governance process.&#x20;
9. Key Protocol Parameter determined through the Governance process are;&#x20;
   1. Intra SuLTV&#x20;
   2. Intra LTV&#x20;
   3. Inter LTV
   4. Mint Limit (User)

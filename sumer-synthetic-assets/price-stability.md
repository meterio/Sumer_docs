# Price Stability

**SuTokens are valued at the price of the underlying USD, ETH, or BTC within the protocol**&#x20;

The Sumer Synthetic Assets (SuTokens) can be minted and repaid to the system for the value of the underlying asset in the lending and borrowing market. This allows arbitragers to balance the demand and supply of the SuTokens in the open market.&#x20;

* If the market price of the SuTokens is above the price target of the native asset, there is an arbitrage opportunity to mint SuTokens. The arbitrageur can place the native asset of equivalent or more value as collateral into the protocol and sell the minted SuToken for a value higher than the native asset in the open market.&#x20;
* If the market price of SuTokens is below the price range of the native asset, then there is an arbitrage opportunity for users who have minted SuTokens to purchase cheaply on the open market and repay their outstanding SuToken liabilities.

Remember, 1:1 minting of SuTokens is only applicable when the minted SuToken is the same as the deposited asset. For cross-asset minting, the collateral ratio is lower. When multiple assets are deposited (ETH, WBTC) to mint a SuToken (SuETH), the protocol by-design enables minting SuToken against a higher collateral ratio first (ETH – SuETH will have a higher collateral ratio than WBTC – SuETH).


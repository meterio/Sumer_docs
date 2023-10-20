# Asset Group Classification

Within the lending and borrowing market, Sumer introduces a concept of asset groups – homogeneous and heterogeneous. Each asset group consists of tokens with similar value, liquidity and risk factor. For example USDC, USDT, BUSD are homogeneous assets and belong to the same asset group whereas USDC and ETH represent heterogeneous asset groups.\


### Homogeneous Group&#x20;

Assets within this group consist of tokens with similar value, liquidity and risk profile.

For e.g.: USDC, USDT, BUSD and SuUSD will represent homogeneous assets within the same group. Alternative stable coins (for e.g.: MIM or FRAX) would not be in the same asset group due to the difference in risk profile when compared to USDC, USDT and BUSD.

### Heterogeneous Group&#x20;

Assets within this group consist of tokens with varying value, liquidity and risk profile.

For e.g.: USDC, ETH and BTC will represent heterogeneous assets.

The understanding of Homogeneous and Heterogeneous groups is critical for a user to determine;&#x20;

1. Applicable collateral limit
2. Applicable Loan-to-Value&#x20;
   1. Intra SuLTV – Depositing native assets to mint SuTokens within the homogeneous group
   2. Intra LTV – Depositing native assets to borrow native asset within the homogeneous group
   3. Inter LTV – Depositing native assets/ SuTokens to borrow native asset or mint SuTokens across heterogeneous group Intra LTV – Depositing SuTokens to borrow native asset or mint SuTokens across homogeneous group&#x20;



Let us understand the homogeneous and heterogeneous groups from below table;

This is in reference to the initial deployment of the protocol on Ethereum and Binance Smart Chain.



<table data-header-hidden><thead><tr><th width="150"></th><th width="150"></th><th width="150"></th><th width="161"></th><th></th><th></th></tr></thead><tbody><tr><td><strong>Supplied Asset</strong></td><td><strong>Network</strong></td><td><strong>Homogeneous native Assets</strong></td><td><strong>Homogeneous Synthetic Asset</strong></td><td><strong>Heterogeneous native Assets</strong></td><td> <strong>Heterogeneous Synthetic Asset</strong> </td></tr><tr><td>USDC</td><td>Ethereum</td><td>USDT</td><td>suUSD</td><td>ETH, WBTC</td><td>suETH, suBTC</td></tr><tr><td>USDT</td><td>Ethereum</td><td>USDC</td><td>suUSD</td><td>ETH, WBTC</td><td>suETH, suBTC</td></tr><tr><td>ETH</td><td>Ethereum</td><td>WETH</td><td>suETH</td><td>USDC, USDT, WBTC</td><td>suUSD, suBTC</td></tr><tr><td>WBTC</td><td>Ethereum</td><td>RenBTC, hBTC</td><td>suBTC</td><td>USDC, USDT, WETH, ETH</td><td>suUSD, suETH</td></tr><tr><td>BUSD</td><td>BSC</td><td>B-USDT</td><td>suUSD</td><td>BNB, B-ETH, B-BTC</td><td>suETH, suBTC</td></tr><tr><td>BNB</td><td>BSC</td><td>-</td><td>-</td><td>BUSD, B-ETH, B-BTC</td><td>suUSD, suBTC, SuETH</td></tr></tbody></table>

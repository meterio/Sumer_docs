# Understanding the applicable mint limit

When multiple native assets are supplied as collateral to mint SuTokens, the system by design gives preference to the homogeneous group over a heterogeneous group while determining the mint limit.

Let us look at a few scenarios;

* **Deposit Asset**

<table data-full-width="true"><thead><tr><th width="132">Deposit</th><th width="157.4736842105263">Intra suLTV</th><th width="135">Intra LTV</th><th width="146">Inter LTV</th><th width="172">Asset Amount</th><th>Collateral Value (USD)</th></tr></thead><tbody><tr><td>USDC</td><td>98.50%</td><td>90%</td><td>80%</td><td>1000</td><td>1000</td></tr><tr><td>ETH</td><td>98.50%</td><td>93%</td><td>80%</td><td>1</td><td>3000</td></tr></tbody></table>

\* These LTV figures are illustrations. Please check protocol parameters for current LTV values

### <mark style="background-color:blue;">**Mint Limit immediately after deposit of asset - SuUSD**</mark>

| SuToken to be minted                   | SuUSD    |
| -------------------------------------- | -------- |
| SuToken minted against Deposit Assets  | 0        |
| Homogeneous Deposit Asset Value (USDC) | 1000 USD |
| Mint Limit @ 98.5% Intra SuLTV         | 985 USD  |
| Heterogenous Deposit Asset Value (ETH) | 3000 USD |
| Mint Limit @80% Inter LTV              | 2400 USD |
| Total Mint Limit Available             | 3385 USD |

### <mark style="background-color:blue;">**Mint Limit immediately after Deposit of asset - SuETH**</mark>

| SuToken to be minted                    | SuETH    |
| --------------------------------------- | -------- |
| SuToken minted against Deposit Assets   | 0        |
| Homogeneous Deposit Asset Value (ETH)   | 3000 USD |
| Mint Limit @ 98.5% Intra SuLTV          | 2955 USD |
| Heterogenous Deposit Asset Value (USDC) | 1000 USD |
| Mint Limit @80% Inter LTV               | 800 USD  |
| Total Mint Limit Available              | 3755 USD |

### <mark style="background-color:blue;">**Mint Limit of SuUSD after minting SuETH**</mark>

| SuToken to be minted                          | SuUSD                     |
| --------------------------------------------- | ------------------------- |
| SuToken already minted against Deposit Assets | SuETH                     |
| Present Value of Minted SuToken               | 0.4925 SuETH (1477.5 USD) |
| Deposit Asset available to Mint (USDC)        | 1000 USDC (1000 USD)      |
| Deposit Asset available to Mint (ETH)         | 0.5 ETH (1500 USD)        |
| Homogeneous Deposit Asset Value (USDC)        | 1000 USD                  |
| Mint Limit @ 98.5% Intra SuLTV                | 985 USD                   |
| Heterogenous Deposit Asset Value (ETH)        | 1500 USD                  |
| Mint Limit @80% Inter LTV                     | 1200 USD                  |
| Total Mint Limit Available                    | 2185 USD                  |
| Overall SuTokens after both Mints             | 2185 SuUSD, 0.4925 SuETH  |

The same determination is made when users are borrowing native assets against a homogeneous or heterogeneous group of Deposit assets.

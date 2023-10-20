# Understanding the applicable mint limit

When multiple native assets are supplied as collateral to mint SuTokens, the system by design gives preference to the homogeneous group over a heterogeneous group while determining the mint limit.

Let us look at a few scenarios;

* **Deposit Asset**



<table data-header-hidden><thead><tr><th width="150"></th><th width="150"></th><th width="150"></th><th width="150"></th><th width="150"></th><th></th></tr></thead><tbody><tr><td><strong>Deposit Asset</strong></td><td><strong>Intra SuLTV</strong></td><td><strong>Intra LTV</strong></td><td><strong>Inter LTV</strong></td><td><strong>Value (native)</strong></td><td><strong>Value (USD)</strong></td></tr><tr><td>USDC</td><td>99.70%</td><td>90%</td><td>70%</td><td>1000</td><td>1000</td></tr><tr><td>ETH</td><td>99.70%</td><td>80%</td><td>70%</td><td>1</td><td>3000</td></tr></tbody></table>

\* These LTV figures are illustrations. Please check protocol parameters for current LTV values



* **Mint Limit immediately after deposit of asset - SuUSD**

| SuToken to be minted                   | SuUSD    |
| -------------------------------------- | -------- |
| SuToken minted against Deposit Assets  | 0        |
| Homogeneous Deposit Asset Value (USDC) | 1000 USD |
| Mint Limit @ 99.7% Intra SuLTV         | 997 USD  |
| Heterogenous Deposit Asset Value (ETH) | 3000 USD |
| Mint Limit @70% Inter LTV              | 2100 USD |
| Total Mint Limit Available             | 3097 USD |

* **Mint Limit immediately after Deposit of asset - SuETH**

| SuToken to be minted                    | SuETH    |
| --------------------------------------- | -------- |
| SuToken minted against Deposit Assets   | 0        |
| Homogeneous Deposit Asset Value (ETH)   | 3000 USD |
| Mint Limit @ 99.7% Intra SuLTV          | 2991 USD |
| Heterogenous Deposit Asset Value (USDC) | 1000 USD |
| Mint Limit @70% Inter LTV               | 700 USD  |
| Total Mint Limit Available              | 3691 USD |

* **Mint Limit of SuUSD after minting SuETH**

| SuToken to be minted                          | SuUSD                     |
| --------------------------------------------- | ------------------------- |
| SuToken already minted against Deposit Assets | SuETH                     |
| Present Value of Minted SuToken               | 0.4985 SuETH (1495.5 USD) |
| Deposit Asset available to Mint (USDC)        | 1000 USDC (1000 USD)      |
| Deposit Asset available to Mint (ETH)         | 0.5 ETH (1500 USD)        |
| Homogeneous Deposit Asset Value (USDC)        | 1000 USD                  |
| Mint Limit @ 99.7% Intra SuLTV                | 997 USD                   |
| Heterogenous Deposit Asset Value (ETH)        | 1500 USD                  |
| Mint Limit @70% Inter LTV                     | 1050 USD                  |
| Total Mint Limit Available                    | 2047 USD                  |
| Overall SuTokens after both Mints             | 2047 SuUSD, 0.4985 SuETH  |

The same determination is made when users are borrowing native assets against a homogeneous or heterogeneous group of Deposit assets.

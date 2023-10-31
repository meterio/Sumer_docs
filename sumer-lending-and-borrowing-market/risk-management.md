---
description: This section has been referenced from AAVE
---

# Risk Management

### <mark style="background-color:blue;">Methodology</mark>

The composability of DeFi enables Sumer Protocol to connect with the rest of the ecosystem and supported networks. However, it also exposes the protocol to financial contagion. Assets used in the protocol affect the protocol at its core, in particular assets accepted as collateral which safeguard the solvency of the protocol. To ensure an asset holds a reasonable amount of risk, we investigate three different levels.

First, we look at smart contract security and counter-parties in governance. If these risks are too high, the assets will be disqualified from the protocol or to be used as collateral. Then we look at market risks, which can be managed via the protocol’s parameters.

#### <mark style="background-color:blue;">Smart Contract Risk</mark>

Smart contract risk focuses on the technical security of an asset based on its underlying code. If one of the supported assets is compromised, collaterals will be affected, threatening the solvency of the protocol. Projects must have undergone audits to be considered, yet smart contract risk is significant, bug bounties can help but it cannot be fully mitigated.

#### <mark style="background-color:blue;">Counterparty Risk</mark>

Counterparty risk assesses qualitatively how and by who the asset is governed. We observe different degrees of governance decentralization that may give direct control over funds (as backing, for example) or attack vectors to the governance architecture which could expose control and funds.

To mitigate the Smart Contract risk and Counterparty risk, Sumer Protocol will only be integrating Blue chip assets in the initial stages of the deployment.

<table data-view="cards"><thead><tr><th></th><th></th><th></th></tr></thead><tbody><tr><td><mark style="color:yellow;"><strong>Arbitrum</strong></mark></td><td></td><td><p>USDC, USDT, DAI</p><p>ETH, wstETH<br>WBTC<br>ARB</p></td></tr><tr><td><mark style="color:yellow;"><strong>Base</strong></mark></td><td></td><td><p>USDC, USDT, DAI</p><p>ETH, wstETH<br>WBTC</p></td></tr><tr><td><mark style="color:yellow;"><strong>Meter</strong></mark></td><td></td><td><p>USDC, USDT</p><p>ETH<br>WBTC<br>MTRG, wstMTRG</p></td></tr></tbody></table>

\*MTRG will be supported due to familiarity of the team with the deployment.

#### <mark style="background-color:blue;">Market Risk</mark>

Market risks are linked to the market size and fluctuations in offer and demand. These risks are particularly relevant for the assets of the protocol: the collateral.&#x20;

If the value of the collateral decreases, it might reach the liquidation threshold and start getting liquidated. The markets then need to hold sufficient volume for these liquidations - sells which tend to lower the price of the underlying asset through slippage affecting the value recovered.

To protect the Protocol against Market risk, below safeguards will be implemented&#x20;

* <mark style="color:yellow;">Flash Loan Attack</mark>

Timelock - Delay in ability to mint SuTokens after the depositing assets are deposited

This will be in addition to protection through Deposit cap of collateralized assets based on availability of on-chain liquidity

* <mark style="color:yellow;">Flash Loan Attack, Price Manipulation</mark>

Deposit Cap and Borrow Cap on assets based on on-chain liquidity available.

Use of Chainlink Oracles (depending on chain, KCC - witnet)

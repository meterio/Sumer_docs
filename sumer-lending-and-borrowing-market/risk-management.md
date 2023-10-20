---
description: This section has been referenced from AAVE
---

# Risk Management

* Methodology

The composability of DeFi enables Sumer Protocol to connect with the rest of the ecosystem and supported networks. However, it also exposes the protocol to financial contagion. Assets used in the protocol affect the protocol at its core, in particular assets accepted as collateral which safeguard the solvency of the protocol. To ensure an asset holds a reasonable amount of risk, we investigate three different levels.

First, we look at smart contract security and counter-parties in governance. If these risks are too high, the assets will be disqualified from the protocol or to be used as collateral. Then we look at market risks, which can be managed via the protocol’s parameters.

* Smart Contract Risk

Smart contract risk focuses on the technical security of an asset based on its underlying code. If one of the supported assets is compromised, collaterals will be affected, threatening the solvency of the protocol. Projects must have undergone audits to be considered, yet smart contract risk is significant, bug bounties can help but it cannot be fully mitigated.

* Counterparty Risk

Counterparty risk assesses qualitatively how and by who the asset is governed. We observe different degrees of governance decentralization that may give direct control over funds (as backing, for example) or attack vectors to the governance architecture which could expose control and funds.

To mitigate the Smart Contract risk and Counterparty risk, Sumer Protocol will only be integrating Blue chip assets in the initial stages of the deployment.

1. Ethereum Network – ETH, WTBC, USDC, USDT - Focus on initial launch&#x20;
2. Binance Smart Chain – BNB. BUSD, USDC, USDT - Focus on initial launch&#x20;
3. KuCoin Community Chain – KCS&#x20;
4. Meter Network – MTRG&#x20;
5. Avalanche – AVAX, USDC (launch not set yet)&#x20;

\*MTRG will be supported due to familiarity of the team with the deployment.

* Market Risk

Market risks are linked to the market size and fluctuations in offer and demand. These risks are particularly relevant for the assets of the protocol: the collateral. If the value of the collateral decreases, it might reach the liquidation threshold and start getting liquidated. The markets then need to hold sufficient volume for these liquidations - sells which tend to lower the price of the underlying asset through slippage affecting the value recovered.

To protect the Protocol against Market risk, below safeguards will be implemented&#x20;

* Flash Loan Attack

Delay in ability to mint SuTokens after the depositing assets are deposited

This protection will not be enabled at the launch of the protocol. The primary approach to protecting the protocol will be driven based on the Deposit cap of collateralized assets based on availability of on-chain liquidity

* Flash Loan Attack, Price Manipulation&#x20;

Cap on Depositing assets based on on-chain liquidity available

All the assets supplied as collateral to Sumer Protocol will have a Deposit cap based on availability of on-chain liquidity. Higher the available liquidity, higher the Deposit cap.

* Flash Loan Attack, Price Manipulation

Use of Chainlink Oracles (depending on chain, KCC - witnet)

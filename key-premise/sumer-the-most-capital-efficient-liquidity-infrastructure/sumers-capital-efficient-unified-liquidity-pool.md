# Sumer's Capital Efficient unified liquidity pool

Sumer introduces a novel risk engine that considers the correlation among assets when underwriting risks.  Unlike traditional lending protocols which determine borrowing power based on assets supplied as collateral, Sumer intelligently matches users’ liability based on the asset supplied as collateral to maximize users’ borrowing power without adding additional risks. Correlated assets in a user position (deposit wstETH, borrow ETH) get significantly higher LTV maximizing capital efficiency and asset utilization than non-correlated assets.

Let us look at a typical use case in DeFI;

<table data-header-hidden><thead><tr><th width="264"></th><th width="139"></th><th width="224"></th><th></th></tr></thead><tbody><tr><td>DeFI User Position</td><td>AAVE E-mode</td><td>Silo/ Isolated Lending</td><td>Sumer</td></tr><tr><td>Deposit wstETH, borrow ETH</td><td>93% LTV</td><td>93-95% LTV</td><td>92% LTV</td></tr></tbody></table>

<figure><img src="../../.gitbook/assets/Sumer correlated non correlated (1).JPG" alt=""><figcaption></figcaption></figure>

Let us now look at the flexibility Sumer providers around typical scenarios surrounding our use case;

<table data-header-hidden><thead><tr><th width="181"></th><th width="207"></th><th width="144"></th><th></th></tr></thead><tbody><tr><td><strong>Scenarios</strong></td><td><strong>AAVE E-mode</strong></td><td><strong>Silo/ Isolated Lending</strong></td><td><strong>Sumer</strong></td></tr><tr><td>User has excess collateral and needs Stable borrowing</td><td>Remove collateral, open new position</td><td>Remove collateral, open new position</td><td>81% LTV with same wstETH collateral</td></tr><tr><td>User has low position health, holds excess stable</td><td>Deposit USDC (75% LTV) to increase health</td><td>Not feasible</td><td>Deposit USDC (82.5% LTV) to increase health</td></tr><tr><td>Increased demand for LRTs, potential looping with wstETH</td><td>Lower LTV for wstETH-LRT looping;  not all assets are supported in e-mode</td><td>Not Feasible</td><td>LRT Users will deposit LRT to borrow wstETH at 90% LTV increasing wstETH yield – a win-win for LRT users and Sumer Users</td></tr><tr><td>Temporary wstETH depeg</td><td>Close Position</td><td>Close Position</td><td>Provide any supported asset as Collateral temporarily</td></tr></tbody></table>

As evident from above, Sumer’s capital efficient unified liquidity pool offers flexibility to users to manage their positions unlike existing lending and borrowing protocols.\

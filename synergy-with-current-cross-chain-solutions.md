# Synergy with current cross-chain solutions

With the introduction of a new multichain asset class, Sumer's focus has been addressing the underlying issue in the key primitive: crypto assets. At its core, Cross-chain solutions address the ‘process’ of transfer while Sumer addresses the ‘product’ to be transferred. This places Sumer in a unique position to enable a synergistic relationship with current cross-chain solutions&#x20;

![](https://lh4.googleusercontent.com/O8SHWbltxLoYyGlQLWs\_858esRIdlPng5w7R7qPHFEaaZHnj9euxo9ygcivuz79ZjbWOuJbM6RwdrV8S08Toe2Xw8fGnuRExPqekqiHuK74vkmVht1IC\_w8Xeu\_Lg46RtWDnuTKsPcHbCkZ0\_A)

When compared to the multi-chain asset class in SuTokens introduced by Sumer to the wrapped tokens approach taken by the current cross-chain solutions, we can understand the value proposition of Sumer better.&#x20;

In the current multichain DeFI ecosystem, the cross-chain solutions have embraced the designs of cross-chain lock/mint bridging or cross-chain swaps.

* **Cross-chain lock/mint bridging solutions**

The cross-chain lock/mint bridging solution requires custodial deposits of native tokens into the bridge contract thereby keeping the deposits idle in the bridge while introducing operational risks of managing the assets through a multi-sig wallet. This is in addition to relying on wrapped tokens (a step away from native tokens) and carrying the risk of non-availability of liquidity on the destination chain for its users and non-composability with smart contracts on the destination chain for its developers.

* **Cross-chain swaps**

Cross-chain swaps provide a partial solution. Cross-chain native swaps like Anyswap provide native token liquidity pools that need to be continually incentivized.  Lack of liquidity leaving users with bridge-provided synthetic assets is a experience once too often. Stargate provides the soft limits and pool rebalancing but loses narrative for critical Layer 1 assets. There is no native ETH beyond Ethereum nor native Avalanche beyond Avalanche C-chain. Other Native chain swaps like Rune require users to lose custody of the asset on the source chain (swapping BTC for Ethereum) and is not an ideal option for users looking to HODL the source chain asset. Swapping back to BTC exposes the user to price fluctuations in the assets.

<table data-header-hidden><thead><tr><th width="298.9807846277022"></th><th width="150"></th><th width="150"></th><th></th></tr></thead><tbody><tr><td><strong>Parameter</strong></td><td><strong>Sumer.Money</strong></td><td><strong>Cross-chain Swaps</strong></td><td> <strong>Lock/Mint Bridges</strong> </td></tr><tr><td>DeFI Users</td><td></td><td></td><td></td></tr><tr><td>Will the bridged token have liquidity on the destination chain?</td><td>✔</td><td>✔</td><td>Maybe</td></tr><tr><td>Are the deposited tokens on the source chain secure; are the smart contracts tamper-proof?</td><td>✔</td><td>-</td><td>Maybe</td></tr><tr><td>Can I earn interest on assets I locked on the original chain?</td><td>✔</td><td>X</td><td>X</td></tr><tr><td>Can I reclaim my native asset back at any time I want to?</td><td>✔</td><td>Maybe</td><td>✔</td></tr><tr><td>DeFi/ Web3 developers</td><td></td><td></td><td></td></tr><tr><td>Will I be able to leverage existing solutions for seamless cross-chain smart contract communication?</td><td>✔</td><td>X</td><td>✔ (Complex)</td></tr><tr><td>Is there a common abstraction for similar assets on different chains?</td><td>✔</td><td>Maybe</td><td>Maybe</td></tr></tbody></table>

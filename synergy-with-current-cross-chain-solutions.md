# Synergy with current cross-chain solutions

<mark style="color:yellow;">With the introduction of a new multichain asset class, Sumer's focus has been addressing the underlying issue in the key primitive: crypto assets.</mark>&#x20;

At its core, Cross-chain solutions address the ‘process’ of transfer while Sumer addresses the ‘product’ to be transferred. This places Sumer in a unique position to enable a synergistic relationship with current cross-chain solutions&#x20;

<figure><img src=".gitbook/assets/Synergy with cross-chain solutions.png" alt=""><figcaption></figcaption></figure>

When compared to the multi-chain asset class in SuTokens introduced by Sumer to the wrapped tokens approach taken by the current cross-chain solutions, we can understand the value proposition of Sumer better.&#x20;

In the current multichain DeFI ecosystem, the cross-chain solutions have embraced the designs of cross-chain lock/mint bridging or cross-chain swaps.

> ### <mark style="background-color:blue;">**Cross-chain lock/mint bridging solutions**</mark>

The cross-chain lock/mint bridging solution <mark style="color:yellow;">requires custodial deposits of native tokens</mark> into the bridge contract thereby keeping the deposits idle in the bridge while introducing <mark style="color:yellow;">operational risks of managing the assets</mark> through a multi-sig wallet. This is in addition to relying on wrapped tokens (a step away from native tokens) and carrying the <mark style="color:yellow;">risk of non-availability of liquidity on the destination chain</mark> for its users and non-composability with smart contracts on the destination chain for its developers.

> ### <mark style="background-color:blue;">**Cross-chain swaps**</mark>

Cross-chain swaps provide a partial solution. Cross-chain native swaps provide <mark style="color:yellow;">native token liquidity pools</mark> <mark style="color:yellow;">that need to be continually incentivized</mark>.  Lack of liquidity leaving users with bridge-provided synthetic assets is a experience once too often. Stargate provides the soft limits and pool rebalancing but loses narrative for critical Layer 1 assets. <mark style="color:yellow;">There is no native ETH beyond Ethereum nor native Avalanche beyond Avalanche C-chain</mark>. Other Native chain swaps like Rune require users to lose custody of the asset on the source chain (swapping BTC for Ethereum) and is not an ideal option for users looking to HODL the source chain asset. Swapping back to BTC exposes the user to price fluctuations in the assets.

<table data-full-width="true"><thead><tr><th width="321.61519429777934">Parameter</th><th width="150">Sumer.Money</th><th width="150">Cross-chain Swaps</th><th> Lock/Mint Bridges </th></tr></thead><tbody><tr><td><mark style="background-color:blue;"><strong>DeFI Users</strong></mark></td><td></td><td></td><td></td></tr><tr><td>Will the bridged token have liquidity on the destination chain?</td><td>✔</td><td>✔</td><td>Maybe</td></tr><tr><td>Are the deposited tokens on the source chain secure; are the smart contracts tamper-proof?</td><td>✔</td><td>-</td><td>Maybe</td></tr><tr><td>Can I earn interest on assets I locked on the original chain?</td><td>✔</td><td>X</td><td>X</td></tr><tr><td>Can I reclaim my native asset back at any time I want to?</td><td>✔</td><td>Maybe</td><td>✔</td></tr><tr><td><mark style="background-color:blue;">DeFi/ Web3 developers</mark></td><td></td><td></td><td></td></tr><tr><td>Will I be able to leverage existing solutions for seamless cross-chain smart contract communication?</td><td>✔</td><td>X</td><td>✔ (Complex)</td></tr><tr><td>Is there a common abstraction for similar assets on different chains?</td><td>✔</td><td>Maybe</td><td>Maybe</td></tr></tbody></table>

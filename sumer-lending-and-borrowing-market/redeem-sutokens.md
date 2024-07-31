# Redeem SuTokens

To maintain Pegging, SuTokens can be redeem to a basket of underlying assets with a redemption fee.  Arbitragers could then help restore SuTokens' price.  There are several aspects related to the redemption process:

### <mark style="background-color:blue;">Redemption Order</mark>

Since SuTokens are minted by users with various collateralized assets, the redemption process goes through each users' account to process the redemption requests. &#x20;

In the current implementation, to reduce the on chain gas consumptions the redemption order is created off chain. The redeemer uses Sumer's backend API to obtain a signed transaction with redemption amount and expiration for the redemption transaction.&#x20;

There are multiple factors impacting your rank in the redemption list, including but not limited to the risk of your position (heterogenous asset group collaterals are more risky than homogeneous group collaterals), whether you are providing liquidity in the pool or sold the SuTokens minted, the liquidity of various collateral pools. &#x20;

### <mark style="background-color:blue;">Redeemable Assets</mark>

Since the minter could use any combination of the supported collateral assets to mint SuTokens, the redemption process may yield a basket of the collaterals that add up to the face value of the SuTokens being redeemed.&#x20;

The protocol will start the redemption from the target minter's assets in the homogeneous asset group and then heterogeneous asset groups until all of the minter's SuToken liability has been redeemed. &#x20;

### <mark style="background-color:blue;">Redemption Fees</mark>

Redemption fees are based on the `BaseRate`, which is dynamically updated. The `BaseRate` increases with each redemption, and decays to 0 over time with a 12 hour half life.

Upon each redemption:

* `BaseRate` is decayed based on time passed since the last fee event
* `BaseRate` is incremented by an amount proportional to the fraction of the total SuToken supply that was redeemed
* The redemption fee is given by `(BaseRate + 0.5%) * CollateralAssets`

`BaseRateNew = BaseRateOld + redeemedsuToken / (2 * totalsuTokenMinted)`

Where `BaseRateOld` is the value just prior to this redemption, and `BaseRateNew` is the new value (and gets applied to this redemption).

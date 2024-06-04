# Redeem SuTokens

To maintain Pegging, SuTokens can be redeem to a basket of underlying assets with a redemption fee.  Arbitragers could then help restore SuTokens' price.  There are several aspects related to the redemption process:

1. Redemption order.  Since suTokens are minted by users with various collateralized assets, the redemption process goes through each users' account to process the redemption requests.  To reduce the on chain gas consumption, Sumer uses an offchain analyzer to decide the order of redemption.  The redeemer has to obtain a signed redemption list from the analyzer to redeem the underlying tokens.  The analyzer may consider various factors including the current liquidity of the protocol, whether a user used heterogenous assets as collaterals, the current debt to asset ratio or risk of the SuToken minters' accounts and even the minter had sold the SuToken into liquidity pools to decide the redemption order.   Since the minter of SuTokens has a significant cost advantage compare to a regular user, it is more cost effective for SuToken minters to purchase to purchase SuTokens at lower cost to pay back their liabilities.
2. Redeemable assets.  Since the minter could use any combination of the supported collateral assets to mint suTokens.  The redemption process will may result a basket of the collaterals that add up to the face value of the suTokens being redeemed.  The protocol will start the redemption from the target minter's assets in the homogeneous asset group and then heterogeneous asset groups until all of the minter's suToken liability has been redeemed. &#x20;
3.  Redemption fees. Redemption fees are based on the `baseRate`, which is dynamically updated. The `baseRate` increases with each redemption, and decays to 0 over time with a 12 hour half life.

    Upon each redemption:

    * `baseRate` is decayed based on time passed since the last fee event
    * `baseRate` is incremented by an amount proportional to the fraction of the total suToken supply that was redeemed
    * The redemption fee is given by `(baseRate + 0.5%) * CollateralAssets`

    `baseRateNew = baseRateOld + redeemedsuToken / (2 * totalsuTokenMinted)`

    Where `baseRateOld` is the value just prior to this redemption, and `baseRateNew` is the new value (and gets applied to this redemption).

This feature is still under development and will be available in Sumer V2 after it is fully audited.  Details will be published soon.&#x20;

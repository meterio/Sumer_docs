# Redeem SuTokens

To maintain Pegging, SuTokens can be redeem to a basket of underlying assets with a redemption fee.  Arbitragers could then help restore SuTokens' price.  There are several aspects related to the redemption process:

1. Redemption order.  Since suTokens are minted by users with various collateralized assets, the redemption process goes through each users' account to process the redemption requests.  The current redemption order in Sumer is based on the outstanding liabilities for each suToken.  For example, the user minted the most amount of suUSD will be the first to handle a new suUSD redemption request.  The order will updated after each redemption.  The rationale is that the minter has a cost advantage (lower buy back price and no redemption fees) by buying back suToken at below peg prices and paying back outstanding suToken liabilities when suToken falls below the target peg.   The biggest suToken minters should pay closer attention to suToken prices.
2. Redeemable assets.  Since the minter could use any combination of the supported collateral assets to mint suTokens.  The redemption process will may result a basket of the collaterals that add up to the face value of the suTokens being redeemed.  The protocol will start the redemption from the target minter's assets in the homogeneous asset group and then heterogeneous asset groups until all of the minter's suToken liability has been redeemed. &#x20;
3.  Redemption fees. Redemption fees are based on the `baseRate`, which is dynamically updated. The `baseRate` increases with each redemption, and decays to 0 over time with a 12 hour half life.

    Upon each redemption:

    * `baseRate` is decayed based on time passed since the last fee event
    * `baseRate` is incremented by an amount proportional to the fraction of the total LUSD supply that was redeemed
    * The redemption fee is given by `(baseRate + 1%) * CollateralAssets`

    `baseRateNew = baseRateOld + redeemedsuToken / (2 * totalsuTokenMinted)`

    Where `baseRateOld` is the value just prior to this redemption, and `baseRateNew` is the new value (and gets applied to this redemption).

This feature is still under development and will be available in Sumer V2 after it is fully audited.  Details will be published soon.&#x20;

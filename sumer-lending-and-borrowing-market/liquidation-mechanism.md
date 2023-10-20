# Liquidation Mechanism

* The liquidation module is a critical component required as a prevention mechanism for bad debts, by paying off loans that have gone beyond its required Collateralization ratio.&#x20;
* This may happen when the collateral decreases in value or the borrowed loan/ minted SuToken increases in value against each other.&#x20;
*   When a liquidation event is triggered, the following events take place:&#x20;

    * The liquidation module will calculate the amount, up to the given asset's Close Factor, required to bring the loan back to a healthy level (i.e. as per the stipulated Collateral Factor)&#x20;
    * A corresponding amount will then be taken from the collateral, calculated at the collateral’s current market price minus a liquidation discount, netted off by a liquidation fee.&#x20;
    * After the said loan amount is repaid, the loan account will be considered a healthy account (within the Collateral Ratio), and will be taken off the liquidation module&#x20;


* The liquidation discount acts as an incentive for arbitrageurs to step in and reduce the borrower’s exposure, thereby reducing the risk of loan default in the process. The amount of liquidation discount (or penalty for borrowers) depends on the asset used as collateral. This liquidation process will be facilitated using the Chainlink price feed (i.e. “oracle”) or supported Oracle service on networks where Sumer is deployed.
* Anyone can participate as a liquidator for Sumer, as long as they are in possession of the corresponding collateral assets.

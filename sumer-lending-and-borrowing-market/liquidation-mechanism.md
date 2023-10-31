# Liquidation Mechanism

The liquidation module is a critical component required as a prevention mechanism for bad debts, by paying off loans that have gone beyond its required Collateralization ratio.&#x20;

### <mark style="background-color:blue;">Health Factor</mark>

The health factor represents the safety of your deposited assets against the borrowed assets/ minted SuTokens and its underlying value. The higher the value is, the safer the state of your funds are against a liquidation scenario.&#x20;

If the health factor reaches 1, liquidation of your deposits will be triggered. A Health Factor below 1 can get liquidated.&#x20;

<mark style="color:yellow;">The health factor depends on the liquidation threshold of your collateral against the value of your borrowed funds.</mark>

### <mark style="background-color:blue;">Liquidation Threshold</mark>

In a compound design,&#x20;

```
Liquidation Threshold = Collateral Rate or LTV
```

### <mark style="background-color:blue;">Liquidation</mark>&#x20;

Liquidation will be triggered when;

```
Value of Borrowed Asset or Minted SuTokens > Value of Supplied Collateral 
```

This is either because the collateral decreases in value or the borrowed loan/ minted SuToken increases in value against each other.&#x20;

When a liquidation event is triggered, the following events take place:&#x20;

* The liquidation module will calculate the amount, up to the given asset's Close Factor, required to bring the loan back to a healthy level (i.e. as per the stipulated Collateral Factor)&#x20;
* A corresponding amount will then be taken from the collateral, calculated at the collateral’s current market price minus a liquidation discount, netted off by a liquidation fee.&#x20;
* After the said loan amount is repaid, the loan account will be considered a healthy account (within the Collateral Ratio), and will be taken off the liquidation module

<mark style="color:yellow;">Anyone can participate as a liquidator for Sumer, as long as they are in possession of the corresponding collateral assets.</mark>

### <mark style="background-color:blue;">Liquidation Incentive</mark>

The liquidation discount acts as an incentive for arbitrageurs to step in and reduce the borrower’s exposure, thereby reducing the risk of loan default in the process.&#x20;

<mark style="color:yellow;">The amount of liquidation discount (or penalty for borrowers) depends on the asset used as collateral.</mark>&#x20;

This liquidation process will be facilitated using the Chainlink price feed (i.e. “oracle”) or supported Oracle service on networks where Sumer is deployed.

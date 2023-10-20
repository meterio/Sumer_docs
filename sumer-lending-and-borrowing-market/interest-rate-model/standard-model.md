# Standard Model

The standard model is used for markets that have relatively lower historical utilization (typically below 80%). Under the standard model, here are how the rates are calculated:&#x20;

* Borrow rate: Base Rate + (Multiplier x Utilization Rate)&#x20;
* Deposit rate: Borrow Rate x Utilization Rate x (1 - Reserve Factor)&#x20;

where

* Base Rate = The minimum (floor) borrowing rate&#x20;
* Multiplier = Scale factor per utilization&#x20;
* Utilization Rate = Asset borrowed / Total asset Deposit&#x20;
* Reserve Factor = Percentage of the spread between Deposit & borrow (the protocol's revenue to be kept in treasury)&#x20;

From the formula, we can see that Utilization Rate is the only dynamic parameter, whereas Base Rate, Multiplier, and Reserve Factor are determined as “constant”.

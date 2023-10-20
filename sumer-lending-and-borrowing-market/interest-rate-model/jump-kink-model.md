# Jump (Kink) Model

The jump (Kink) Model is a formula that is used for markets that have typically higher historical utilization. The resulting interest rate in this model will be significantly higher than that under the Standard Model regime to encourage heavier deposits and discourage further borrowing.&#x20;

* Borrow Rate: Base Rate + \[Multiplier x min(Kink, Utilization)] + \[Jump Multiplier x max(0, Utilization - Kink)&#x20;
* Deposit rate: Borrow Rate x Utilization Rate x (1 - Reserve Factor)&#x20;

where&#x20;

* Kink = The cut-off point in utilization rate where interest rate follows the Jump Model (e.g., 80%)&#x20;
* Jump Multiplier = Scale factor per utilization under Jump Model&#x20;
* Base Rate = The minimum (floor) borrowing rate&#x20;
* Multiplier = Scale factor per utilization&#x20;
* Utilization Rate = Asset borrowed / Total asset Deposit


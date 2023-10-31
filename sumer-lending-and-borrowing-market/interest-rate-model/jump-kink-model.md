# Jump (Kink) Model

The jump (Kink) Model is a formula that is used for markets that have typically higher historical utilization. The resulting interest rate in this model will be significantly higher than that under the Standard Model regime to encourage heavier deposits and discourage further borrowing.&#x20;

### <mark style="background-color:blue;">Borrow rate</mark>

```
Base Rate 
+ 
[Multiplier * min(Kink, Utilization)] 
+  
[Jump Multiplier * max(0, Utilization - Kink)]
```

### <mark style="background-color:blue;">Deposit rate</mark>&#x20;

```
Borrow Rate x Utilization Rate x (1 - Reserve Factor) 
```

The Key Parameters are defined as below;

#### <mark style="background-color:blue;">Kink</mark>

The cut-off point in utilization rate where interest rate follows the Jump Model (e.g., 80%)

#### <mark style="background-color:blue;">Base Rate</mark>&#x20;

The minimum (floor) borrowing rate&#x20;

#### <mark style="background-color:blue;">Base Rate</mark>&#x20;

The minimum (floor) borrowing rate&#x20;

#### <mark style="background-color:blue;">Multiplier</mark>

&#x20;Scale factor per utilization&#x20;

#### <mark style="background-color:blue;">Utilization Rate</mark>&#x20;

Total Assets borrowed / Total assets Deposited&#x20;

#### <mark style="background-color:blue;">Reserve Factor</mark>&#x20;

Percentage of the spread between Deposit & borrow (the protocol's revenue to be kept in treasury)&#x20;

From the formula, we can see that Utilization Rate is the only dynamic parameter, whereas Base Rate, Multiplier, and Reserve Factor are determined as “constant”.




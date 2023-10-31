# Standard Model

The standard model is used for markets that have relatively lower historical utilization (typically below 80%). Under the standard model, here are how the rates are calculated:&#x20;

### <mark style="background-color:blue;">Borrow rate</mark>

Base Rate + (Multiplier x Utilization Rate)&#x20;

```
Base Rate 
+ 
(Multiplier x Utilization Rate) 
```

### <mark style="background-color:blue;">Deposit rate</mark>&#x20;

```
Borrow Rate x Utilization Rate x (1 - Reserve Factor) 
```

The Key Parameters are defined as below;

#### <mark style="background-color:blue;">Base Rate</mark>&#x20;

The minimum (floor) borrowing rate&#x20;

#### <mark style="background-color:blue;">Multiplier</mark>

&#x20;Scale factor per utilization&#x20;

#### <mark style="background-color:blue;">Utilization Rate</mark>&#x20;

Total Assets borrowed / Total assets Deposited&#x20;

#### <mark style="background-color:blue;">Reserve Factor</mark>&#x20;

Percentage of the spread between Deposit & borrow (the protocol's revenue to be kept in treasury)&#x20;

From the formula, we can see that Utilization Rate is the only dynamic parameter, whereas Base Rate, Multiplier, and Reserve Factor are determined as “constant”.

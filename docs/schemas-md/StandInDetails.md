
# StandInDetails

| *description*: | *Indicates standin transaction.*|
|----|----|
| standInType* |    ``` string ```   *example: FIXED_AMOUNT* Indicates standin instruction type. Enum:[ FIXED_AMOUNT, MAXIMUM_AMOUNT ]|
| numberOfDebits* |    ``` string ```   *pattern: (UN)|(ND)|([0-9]{2}) example: 12* Indicates number of standin instruction debits.Possible values can be two digit number or UN (Until it is cancelled) or ND (Not defined).|
| siValidated* |    ``` boolean ```   *example: true* Indicates standin instruction validation flag, it can be true or false. "false" - Not validated, "true" - Validated.|
| maximumTransactionAmount* |    ``` number ```   *example: 1800* Maximum debit amount per standin instruction transaction.|
| siHubId* |    ``` string ```   *maxLength: 10 example: Y3PCO6QGHT* Unique identifier for standin instruction.|
| frequency |    ``` string ```   *example: MONTHLY* Indicates frequency of the standin instruction debit. Enum:[ DAILY, TWICEWEEKLY, WEEKLY, TENDAYS, FORTNIGHTLY, MONTHLY, EVERYTWOMONTHS, TRIMESTER, QUARTERLY, HALFYEARLY, YEARLY, UNSCHEDULED ]|

**StandInDetails Example:**

```{r}

{
  "standInType": "FIXED_AMOUNT",
  "numberOfDebits": "12",
  "siValidated": true,
  "maximumTransactionAmount": 1800,
  "siHubId": "Y3PCO6QGHT",
  "frequency": "MONTHLY"
}
```  







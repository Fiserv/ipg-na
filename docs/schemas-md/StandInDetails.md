
# StandInDetails

| *description*: | *Indicates standin transaction.*|
|----|----|
| standInType* |    ``` string ```  <br/>   *example: FIXED_AMOUNT*  <br/> Indicates standin instruction type. <br/>  Enum:[ FIXED_AMOUNT, MAXIMUM_AMOUNT ]|
| numberOfDebits* |    ``` string ```  <br/>   *pattern: (UN)|(ND)|([0-9]{2})  <br/> example: 12*  <br/> Indicates number of standin instruction debits.Possible values can be two digit number or UN (Until it is cancelled) or ND (Not defined).|
| siValidated* |    ``` boolean ```   <br/>  *example: true* <br/>  Indicates standin instruction validation flag, it can be true or false. "false" - Not validated, "true" - Validated.|
| maximumTransactionAmount* |    ``` number ```  <br/>   *example: 1800*  <br/> Maximum debit amount per standin instruction transaction.|
| siHubId* |    ``` string ```   <br/>  maxLength: 10  <br/> *example: Y3PCO6QGHT*  <br/> Unique identifier for standin instruction.|
| frequency |    ``` string ```   <br/>  *example: MONTHLY*  <br/> Indicates frequency of the standin instruction debit.  <br/> Enum:[ DAILY, TWICEWEEKLY, WEEKLY, TENDAYS, FORTNIGHTLY, MONTHLY, EVERYTWOMONTHS, TRIMESTER, QUARTERLY, HALFYEARLY, YEARLY, UNSCHEDULED ]|

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







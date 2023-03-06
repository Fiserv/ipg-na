
# RequiredConsumerData

| *description*:   | *Provides details for data requested from the payer.*|
|----|----|
| hint |    ``` string ```   <br/> *maxLength: 2048* <br/>  Description of required data that need to be provided.|
| validationExpression |    ``` string ```  <br/>  *maxLength: 2048* <br/>  Regexp validation expression for requested data.|
| key |  ``` string ``` <br/>   *maxLength: 2048* <br/>  Key for required data item.|

**RequiredConsumerData Example:**

```{r}

{
  "hint": "Your 6-digit Code will be provided in your mobile application",
  "validationExpression": "^\\\\d{6}$",
  "key": "BLIK_CODE"
}
```




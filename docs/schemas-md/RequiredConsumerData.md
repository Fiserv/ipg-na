
# RequiredConsumerData

| *description*:   | *Provides details for data requested from the payer.*|
|----|----|
| hint |    ``` string ```  *maxLength: 2048*. Description of required data that need to be provided.|
| validationExpression |    ``` string ```  *maxLength: 2048*. Regexp validation expression for requested data.|
| key |  ``` string ```  *maxLength: 2048*. Key for required data item.|

**RequiredConsumerData Example:**

```{r}

{
  "hint": "Your 6-digit Code will be provided in your mobile application",
  "validationExpression": "^\\\\d{6}$",
  "key": "BLIK_CODE"
}
```





# CurrencyConversion

| *description*:   | *Currency conversion. Abstract class, do not use this class directly, use one of its children: Dcc, DynamicPricing.*|
|----|----|
| conversionType* |    ``` string ``` <br/> *example: Dcc*  <br/>  Type of currency conversion.|
| inquiryRateId* |    ``` string ```  <br/> *pattern: ^(?!\s*$).+  <br/>  *example: 123456* <br/> Inquiry rate id.|

**CurrencyConversion Example:**

```{r}

{
  "conversionType": "Dcc",
  "inquiryRateId": "123456",
  "dccApplied": true
}
```


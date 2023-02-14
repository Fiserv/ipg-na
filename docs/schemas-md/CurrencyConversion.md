
# CurrencyConversion

| *description*:   | *Currency conversion. Abstract class, do not use this class directly, use one of its children: Dcc, DynamicPricing.*|
|----|----|
| conversionType* |    ``` string ```  *example: Dcc*  Type of currency conversion.|
| inquiryRateId* |    ``` string ```  *pattern: ^(?!\s*$).+ example: 123456* Inquiry rate id.|


**CurrencyConversion Example:**

```{r}

{
  "conversionType": "Dcc",
  "inquiryRateId": "123456",
  "dccApplied": true
}
``` 

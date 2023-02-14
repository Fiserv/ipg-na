
# Dcc

| *description*:   | *Request to perform a dynamic pricing exchange rate inquiry.*|
|----|----|
| conversionType* |    ``` string ```  *example: Dcc* Type of currency conversion.|
| inquiryRateId* |    ``` string ```  *pattern: ^(?!\s*$).+ example: 123456* Inquiry rate id.|
| dccApplied |   ``` string ```  *example: true* Indicates whether customer agrees with rate to be used.|

**Dcc Example:**

```{r}

{
  "conversionType": "Dcc",
  "inquiryRateId": "123456",
  "dccApplied": true
}
``` 

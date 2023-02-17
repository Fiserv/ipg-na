
# Dcc

| *description*:   | *Request to perform a dynamic pricing exchange rate inquiry.*|
|----|----|
| conversionType* |    ``` string ``` <br/> *example: Dcc*  <br/> Type of currency conversion.|
| inquiryRateId* |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+ example: 123456*  <br/> Inquiry rate id.|
| dccApplied |   ``` string ```  <br/>  *example: true*  <br/> Indicates whether customer agrees with rate to be used.|

**Dcc Example:**

```{r}

{
  "conversionType": "Dcc",
  "inquiryRateId": "123456",
  "dccApplied": true
}
``` 

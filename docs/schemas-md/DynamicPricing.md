
# DynamicPricing

| *description*:   | *Request to perform a dynamic pricing exchange rate inquiry.*|
|----|----|
| conversionType* |    ``` string ```  *example: Dcc* Type of currency conversion.|
| inquiryRateId* |    ``` string ```  *pattern: ^(?!\s*$).+ example: 123456* Inquiry rate id.|
| foreignCurrency |   ``` string ```  *pattern: ([A-Z]{3})|([0-9]{3}) example: 978* The currency code to convert for dynamic pricing in ISO 4217 currency code format.|
| foreignAmount |   ``` string ```  *pattern: ^(?!\s*$).+ example: 22.52* Foreign amount.|


**DynamicPricing Example:**

```{r}

{
  "conversionType": "DynamicPricing",
  "inquiryRateId": "123456",
  "foreignCurrency": "978",
  "foreignAmount": "22.52"
}
``` 

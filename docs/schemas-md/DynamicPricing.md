
# DynamicPricing

| *description*:   | *Request to perform a dynamic pricing exchange rate inquiry.*|
|----|----|
| conversionType* |    ``` string ```  <br/>  *example: Dcc*  <br/> Type of currency conversion.|
| inquiryRateId* |    ``` string ```  <br/>  pattern: ^(?!\s*$).+  <br/> example: 123456* <br/>  Inquiry rate id.|
| foreignCurrency |   ``` string ```   <br/>  *pattern: ([A-Z]{3})|([0-9]{3})  <br/> example: 978*  <br/> The currency code to convert for dynamic pricing in ISO 4217 currency code format.|
| foreignAmount |   ``` string ```  <br/>  *pattern: ^(?!\s*$).+  <br/> example: 22.52*  <br/> Foreign amount.|


**DynamicPricing Example:**

```{r}

{
  "conversionType": "DynamicPricing",
  "inquiryRateId": "123456",
  "foreignCurrency": "978",
  "foreignAmount": "22.52"
}
``` 

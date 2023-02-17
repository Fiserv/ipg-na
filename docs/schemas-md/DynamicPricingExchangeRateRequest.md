
# DynamicPricingExchangeRateRequest

| *description*:   | *Request to perform a dynamic pricing exchange rate inquiry.*|
|----|----|
| requestType* |    ``` string ```  <br/>  *example: DynamicPricingExchangeRateRequest*  <br/> Object name of the exchange rate request. |
| baseAmount* |    ``` number ```  <br/>  *example: 12.32*  <br/> The original amount of the merchant currency for calculation.|
| foreignCurrency |   ``` string ```  <br/> maxLength: 3  <br/> pattern: ([A-Z]{3})|([0-9]{3})  <br/> *example: USD*  <br/> The currency code to convert for dynamic pricing in either numeric or alphabetic ISO 4217 currency code format.|

**DynamicPricingExchangeRateRequest Example:**

```{r}

{
  "requestType": "DynamicPricingExchangeRateRequest",
  "baseAmount": 12.32,
  "foreignCurrency": "USD"
}
``` 

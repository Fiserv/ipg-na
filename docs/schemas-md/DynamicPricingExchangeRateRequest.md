
# DynamicPricingExchangeRateRequest

| *description*:   | *Request to perform a dynamic pricing exchange rate inquiry.*|
|----|----|
| requestType* |    ``` string ```  *example: DynamicPricingExchangeRateRequest* Object name of the exchange rate request. |
| baseAmount* |    ``` number ```  *example: 12.32* The original amount of the merchant currency for calculation.|
| foreignCurrency |   ``` string ```  *maxLength: 3 pattern: ([A-Z]{3})|([0-9]{3}) example: USD* The currency code to convert for dynamic pricing in either numeric or alphabetic ISO 4217 currency code format.|

**DynamicPricingExchangeRateRequest Example:**

```{r}

{
  "requestType": "DynamicPricingExchangeRateRequest",
  "baseAmount": 12.32,
  "foreignCurrency": "USD"
}
``` 

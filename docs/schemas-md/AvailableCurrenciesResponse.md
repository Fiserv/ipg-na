
# AvailableCurrenciesResponse

| *description*: | *List of available currencies for a store.*|
|----|----|
| clientRequestId |    ``` string ```   *example: 30dd879c-ee2f-11db-8314-0800200c9a66* Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```   *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7* Request identifier in API, can be used to request logs from the support team.|
| responseType | [ResponseType](?path=docs/schemas-md/ResponseType.md)|  
| currencies | [StoreCurrency](?path=docs/schemas-md/StoreCurrency.md)|

**AvailableCurrenciesResponse Example:**

```{r}

{
  "clientRequestId": "30dd879c-ee2f-11db-8314-0800200c9a66",
  "apiTraceId": "rrt-0bd552c12342d3448-b-ea-1142-12938318-7",
  "currencies": [
    {
      "literalCurrencyCode": "USD",
      "numericCurrencyCode": 840,
      "decimalPlaces": 2,
      "defaultCurrency": true
    },
    {
      "literalCurrencyCode": "EUR",
      "numericCurrencyCode": 978,
      "decimalPlaces": 2,
      "defaultCurrency": false
    }
  ]
}
```







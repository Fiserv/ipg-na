
# StoreCurrency

| *description*: | *Currency details associated with a store.*|
|----|----|
| literalCurrencyCode |    ``` string ```  <br/> *example: USD* <br/> This field contains the ISO alpha currency code.|
| numericCurrencyCode |    ``` string ```  <br/> *example: 840* <br/> This field contains the ISO numeric currecy code.|
| decimalPlaces |    ``` integer ```  <br/> ($int32) <br/> example: 2* <br/> This field indicates the number of decimal places required for this currency.|
| defaultCurrency |    ``` boolean ```  <br/> *example: true* <br/> This field indicates if this currency is the default currency for queried store.|

**StoreCurrency Example:**

```{r}

{
  "literalCurrencyCode": "USD",
  "numericCurrencyCode": "840",
  "decimalPlaces": 2,
  "defaultCurrency": true
}
```  






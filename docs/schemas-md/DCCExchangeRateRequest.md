
# DCCExchangeRateRequest

| *description*:   | *Request to perform a DCC exchange rate inquiry.*|
|----|----|
| requestType* |    ``` string ``` <br/> *example: DCCExchangeRateRequest*  <br/> Object name of the exchange rate request. |
| baseAmount* |    ``` number ```  <br/>  *example: 12.32*  <br/> The original amount of the merchant currency for calculation.|
| storeId |   ``` string ```  <br/>  *maxLength: 20 example: 1109959991*  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| bin | ```string```  <br/>  *pattern: [0-9]{6,11} example: 411111*  <br/> The bank identification number (BIN) of the card to be used for DCC. The BIN is the first 6-11 digits of the card number.|        

**DCCExchangeRateRequest Example:**

```{r}

{
  "requestType": "DCCExchangeRateRequest",
  "baseAmount": 12.32,
  "bin": "411111"
}
``` 

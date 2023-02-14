
# PaymentDevice

| *description*:   | *Information from the payment device including the blob data and its mode of entry.*|
|----|----|
| deviceType* |    ``` string ```  *example: SWIPE* The data format. Enum:[ SWIPE ]|
| data* |    ``` string ```  *pattern: ^(?!\s*$).+ example: 02A600C0170018008292;5424********1732=1810?*B73CD8C26233D4FFEC5500ED394439D97DDA5F530942D21D0000000000000000000000000000000000000000363434543035353734326299492410027300000260DC03*  Data from device containing, at a minimum, a transaction-unique key serial number (KSN) and track 2 card data.|
| securityCode |    ``` string ```  *minLength: 3 maxLength: 4 example: 977* Card verification value/number.|
| cardholderName |    ``` string ```  *example: Gary Jablonski* Name of cardholder.|
| cardFunction | [CardFunction](?path=docs/schemas-md/CardFunction.md)|

**PaymentDevice Example:**

```{r}

{
    "deviceType": "SWIPE",
    "data": "02A600C0170018008292;5424********1732=1810?*B73CD8C26233D4FFEC5500ED394439D97DDA5F530942D21D0000000000000000000000000000000000000000363434543035353734326299492410027300000260DC03",
    "securityCode": "977"
}
```  
  


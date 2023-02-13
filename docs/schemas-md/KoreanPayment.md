
# KoreanPayment

| *description*:   | *The payment object for AliPay transactions. Use this to populate AliPay payment method details*|
|----|----|
| billKeyId* |    ``` string ```   *maxLength: 28* |
| entry |    ``` string ```   *example: web* Enum:Array [ 2 ] - [ mobile, web ]|
| billType |    ``` string ```   *example: TAX_FREE*  Enum:Array [ 2 ] - [ TAXABLE, TAX_FREE ]|


**KoreanPayment Example:**

```{r}

{
  "billKeyId": "testipg5000000",
  "entry": "web",
  "billType": "TAX_FREE"
}
```






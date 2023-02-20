
# KoreanPayment

| *description*:   | *The payment object for AliPay transactions. Use this to populate AliPay payment method details*|
|----|----|
| billKeyId* |    ``` string ```  <br/>   *maxLength: 28* |
| entry |    ``` string ```   <br/>  *example: web*  <br/> Enum:Array [ 2 ] - [ mobile, web ]|
| billType |    ``` string ```  <br/>   *example: TAX_FREE*   <br/> Enum:Array [ 2 ] - [ TAXABLE, TAX_FREE ]|


**KoreanPayment Example:**

```{r}

{
  "billKeyId": "testipg5000000",
  "entry": "web",
  "billType": "TAX_FREE"
}
```






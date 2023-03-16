
# UsePaymentToken

| *description*:   | *Payment token usage details.*|
|----|----|
| value |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+  <br/>  example: 1235325235236* <br/>  Client-supplied payment token value.|
| tokenOriginStoreId |    ``` string ```   <br/> *maxLength: 20  <br/>  example: 12345500001* <br/>  The ID of a same store (or) sibling store in a hierarchy for which the token was originally created.|
| function | CardFunction   ``` string ``` <br/>   *example: DEBIT* <br/>  Card function. This field is required when performing transactions for Brazil merchants.  <br/> Enum:    > Array [ 5 ] - [ CREDIT, DEBIT, PREPAID, VOUCHER, UNDEFINED ]|
| securityCode |    ``` string ```   <br/> *minLength: 3  <br/>  minLength: 3  <br/>  example: 977*. Card verification value/number.|
| expiryDate |  [Expiration](?path=docs/schemas-md/Expiration.md)|  
| **UpdatePaymentToken Example** | ```  { "value": "3425345345yygg", "reusable": true, "declineDuplicates": false, "paymentCard": {   "number": "5424180279791732", "expiryDate": { "month": "12", "year": "24","securityCode": "977" } } } ``` |    

**UsePaymentToken Example:**

```{r}

{
  "value": "1235325235236",
  "tokenOriginStoreId": "12345500001",
  "function": "DEBIT",
  "securityCode": "977",
  "expiryDate": {
    "month": "12",
    "year": "24"
  }
}
```

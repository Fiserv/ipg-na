
# UpdatePaymentToken

| *description*:   | *Use this model to Update payment token.*|
|----|----|
| value |    ``` string ```  <br/>  *example:  234ljl124l12* <br/>  Client-supplied payment token value. Only applicable for DataVault tokenization scheme.|
| reusable |    ``` boolean ```  <br/>  *default: true  <br/>  example: true* <br/> If the token is reusable.|
| declineDuplicates |    ``` boolean ```   <br/> *default: false  <br/>  example: false* <br/> Decline duplicate payment info if client token is supplied.|   
| paymentCard | [PaymentCard](?path=docs/schemas-md/PaymentCard.md)|  

**UpdatePaymentToken Example:**

```{r}

{
  "value": "3425345345yygg",
  "reusable": true,
  "declineDuplicates": false,
  "paymentCard": {
    "number": "5424180279791732",
    "expiryDate": {
      "month": "12",
      "year": "24",
      "securityCode": "977"
    }
  }
}
```
 




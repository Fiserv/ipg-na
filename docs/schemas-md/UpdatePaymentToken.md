
# UpdatePaymentToken

| *description*:   | *Use this model to Update payment token.*|
|----|----|
| value |    ``` string ```  *example:  234ljl124l12*. Client-supplied payment token value. Only applicable for DataVault tokenization scheme.|
| reusable |    ``` boolean ```  *default: true  example: true*. If the token is reusable.|
| declineDuplicates |    ``` boolean ```  *default: false  example: false*. Decline duplicate payment info if client token is supplied.|   
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
 




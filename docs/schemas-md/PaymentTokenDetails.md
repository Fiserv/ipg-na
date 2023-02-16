
# PaymentTokenDetails

| *description*:   | *Response details for payment token creation.*|
|----|----|
| value |    ``` string ```  <br/> *example:  234ljl124l12*.  <br/> Client-supplied payment token value. Only applicable for DataVault tokenization scheme.|
| reusable |    ``` boolean ```  <br/>  default: true  <br/> *example: true*.  <br/> If the token is reusable.|
| declineDuplicates |    ``` boolean ```   <br/> default: false   <br/> *example: false*.  <br/> Decline duplicate payment info if client token is supplied.|
| last4 |    ``` string ```  <br/>  *example: 4997*.  <br/> The last 4 numbers of a payment card.|
| brand |    ``` string ```   <br/> *example: VISA*.  <br/> Card brand, only for tokenization with payment.|
| accountVerification |    ``` boolean ```  <br/>  *example: true*.  <br/> If the account the token was created from has been verified.|
| type |    ``` string ```  *example: PAYMENT_CARD*.  <br/> Indicates the type of tokenization source.|
| error | [Error](?path=docs/schemas-md/Error.md)|    

**PaymentTokenDetails Example:**

```{r}

{
  "value": "234ljl124l12",
  "reusable": true,
  "declineDuplicates": false,
  "last4": "4997",
  "brand": "VISA",
  "accountVerification": true,
  "type": "PAYMENT_CARD"
}
```


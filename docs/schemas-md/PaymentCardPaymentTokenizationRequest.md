
# PaymentCardPaymentTokenizationRequest

| *description*:   | *Used to generate payment tokens during payment.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentCardPaymentTokenizationRequest*  <br/>  Object name of the payment schedules request.|
| storeId |    ``` string ```  <br/> maxLength: 20   <br/> *example: 12345500000*  <br/>  An optional outlet ID for clients that support multiple stores in the same app.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|
| accountVerification |  ``` boolean ```  <br/>  default: false  <br/>  *example: true*  <br/>  If the account should be verified prior to token creation.|
| merchantTransactionId |    ``` string ```  <br/> maxLength: 40  <br/> *example: lsk23532djljff3*  <br/>  The unique merchant transaction ID from the request, if supplied.|
| additionalDetails | [AdditionalDetails](?path=docs/schemas-md/AdditionalDetails.md)|
| paymentCard | [PaymentCard](?path=docs/schemas-md/PaymentCard.md)|  
  

**PaymentCardPaymentTokenizationRequest Example:**

```{r}

{
  "requestType": "PaymentCardPaymentTokenizationRequest",
  "paymentCard": {
    "number": "4035874000424977",
    "expiryDate": {
      "month": "12",
      "year": "25"
    },
    "securityCode": "977"
  },
  "billingAddress": {
    "address1": "5565 Glenridge Conn",
    "city": "Atlanta",
    "postalCode": "30342",
    "country": "USA"
  },
  "createToken": {
    "value": "234ljl124l12",
    "reusable": true,
    "declineDuplicates": false
  },
  "accountVerification": true
}
```



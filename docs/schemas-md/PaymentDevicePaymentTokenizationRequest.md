
# PaymentDevicePaymentTokenizationRequest

| *description*:   | *Used to generate payment tokens during payment using a payment device.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentDevicePaymentTokenizationRequest* <br/> Object name of the payment schedules request.|
| storeId |    ``` string ```   <br/> maxLength: 20   <br/> *example: 12345500000*  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|
| createToken | [CreatePaymentToken](?path=docs/schemas-md/CreatePaymentToken.md)|
| accountVerification |  ``` boolean ```  <br/>  *default: false  example: true*  <br/> If the account should be verified prior to token creation.|
| merchantTransactionId |    ``` string ```  <br/> maxLength: 40  <br/> *example: lsk23532djljff3* <br/> The unique merchant transaction ID from the request, if supplied.|
| additionalDetails | [AdditionalDetails](?path=docs/schemas-md/AdditionalDetails.md)|
| paymentDevice |  [PaymentDevice](?path=docs/schemas-md/PaymentDevice.md)|     

**PaymentDevicePaymentTokenizationRequest Example:**

```{r}

{
  "requestType": "PaymentDevicePaymentTokenizationRequest",
  "paymentDevice": {
    "deviceType": "SWIPE",
    "data": "02A600C0170018008292;5424********1732=1810?*B73CD8C26233D4FFEC5500ED394439D97DDA5F530942D21D0000000000000000000000000000000000000000363434543035353734326299492410027300000260DC03",
    "securityCode": "977",
    "cardholderName": "First Cardholder",
    "cardFunction": "CREDIT",
    "brand": "VISA"
  },
  "billingAddress": {
    "address1": "5565 Glenridge Conn",
    "city": "Atlanta",
    "postalCode": "30342",
    "country": "USA"
  },
  "createToken": {
    "value": "234ljl124l122",
    "reusable": true,
    "declineDuplicates": false
  },
  "accountVerification": true
}
```





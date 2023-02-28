
# PaymentDeviceCreditTransaction

| *description*:   | *Request to create credit transaction using decrypted card details from payment device.  <br/> The transaction origin will be fixed as PHONE when data is manually entered into the device and as RETAIL when data is entered into the device via swipe.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentDeviceCreditTransaction*  <br/> Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  <br/>  maxLength: 20  <br/>  *example: 12345500000*. <br/>  An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```  <br/>   * maxLength: 40  <br/> example: lsk23532djljff3*. <br/>  The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md)  <br/>  ``` string ```   <br/> *example: ECOM*  <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face).  <br/> Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ```  <br/> ($int64)  <br/>  *example: 838916029301*.  <br/> The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  <br/>  *example: true*.  <br/> Indicates if the particular transaction is a partial approval transaction, if supplied.|
| paymentMethod | [PaymentDevicePaymentMethod](?path=docs/schemas-md/PaymentDevicePaymentMethod.md)|

**PaymentDeviceCreditTransaction Example:**

```{r}

{
  "requestType": "PaymentDeviceCreditTransaction",
  "transactionAmount": {
    "total": 12.04,
    "currency": "USD"
  },
  "paymentMethod": {
    "paymentDevice": {
      "deviceType": "SWIPE",
      "data": "02A600C0170018008292;5424********1732=1810?*B73CD8C26233D4FFEC5500ED394439D97DDA5F530942D21D0000000000000000000000000000000000000000363434543035353734326299492410027300000260DC03",
      "securityCode": "977",
      "cardholderName": "First Cardholder",
      "cardFunction": "CREDIT",
      "brand": "VISA"
    }
  }
}
```  


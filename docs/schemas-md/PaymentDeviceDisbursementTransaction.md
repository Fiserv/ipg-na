
# PaymentDeviceDisbursementTransaction

| *description*:   | *Request to create disbursement transaction using decrypted card details from payment device. The transaction origin will be fixed as PHONE when data is manually entered into the device and as RETAIL when data is entered into the device via swipe.*|
|----|----|
| requestType |    ``` string ```  *example:   PaymentCardCreditTransaction*.Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  TransactionOrigin  ``` string ```  *example: ECOM*.The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ``` ($int64)  *example: 838916029301*. The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  *example: true*. Indicates if the particular transaction is a partial approval transaction, if supplied.|
| paymentMethod | [PaymentDevicePaymentMethod](?path=docs/schemas-md/PaymentDevicePaymentMethod.md)|
| disbursement | [Disbursement](?path=docs/schemas-md/Disbursement.md)|

**PaymentDeviceDisbursementTransaction Example:**

```{r}

{
  "requestType": "PaymentDeviceDisbursementTransaction",
  "transactionAmount": {
    "total": "50",
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
  },
  "disbursement": {
    "disbursementType": "FundingTransactionType",
    "senderInfo": {
      "name": "Franklin Sender Roosevelt",
      "streetAddress": "5565 Glenridge Connector",
      "city": "Atlanta",
      "stateCode": "GA",
      "countryCode": "US",
      "postalCode": "30342",
      "phoneNumber": "4044040740",
      "birthDate": "19560121",
      "referenceNumber": "12345678",
      "accountNumber": "135246"
    },
    "receiverInfo": {
      "name": "Abraham Receiver Lincoln",
      "streetAddress": "5565 Glenridge Connector",
      "city": "Atlanta",
      "stateCode": "GA",
      "countryCode": "US",
      "postalCode": "30342",
      "phoneNumber": "4044040740",
      "referenceNumber": "12345678",
      "accountNumber": "135246"
    }
  }
}
```  

  

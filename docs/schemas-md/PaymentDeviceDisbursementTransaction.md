
# PaymentDeviceDisbursementTransaction

| *description*:   | *Request to create disbursement transaction using decrypted card details from payment device.  <br/> The transaction origin will be fixed as PHONE when data is manually entered into the device and as RETAIL when data is entered into the device via swipe.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentDeviceDisbursementTransaction* <br/> Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  <br/> maxLength: 20  <br/> *example: 12345500000*.  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```  <br/> maxLength: 40  <br/> *example: lsk23532djljff3*.  <br/> The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md)  <br/>  ``` string ```   <br/> *example: ECOM*  <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face).  <br/> Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ```  <br/>  ($int64)  <br/>  *example: 838916029301* <br/> The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  <br/>  *example: true* <br/> Indicates if the particular transaction is a partial approval transaction, if supplied.|
| paymentMethod | [PaymentDevicePaymentMethod](?path=docs/schemas-md/PaymentDevicePaymentMethod.md)|
| disbursement | [Disbursement](?path=docs/schemas-md/Disbursement.md)|
| authenticationResult | [AuthenticationResult](?path=docs/schemas-md/AuthenticationResult.md)| 

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
      "accountNumber": "135246",
      "accountType": "CARD_ACCOUNT_NO"
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
      "accountNumber": "135246",
      "accountType": "ROUTING_TRANSIT_NO_AND_BANK_ACCOUNT_NO"
    }
  },
  "order": {
    "purposeOfPaymentCode": "ISCCRD",
    "additionalDetails": {
      "comments": "Payment Device Disbursement Transaction",
      "invoiceNumber": "984424645416",
      "purchaseOrderNumber": "4545623458",
      "businessApplicationIdentifier": "ACCOUNT_TO_ACCOUNT",
      "transactionTypeIdentifier": "BUSINESS_DISBURSEMENT_MONEY_SEND"
    }
  },
  "authenticationResult": {
      "authenticationType": "Secure3D21AuthenticationResult",
      "cavv": "AAABBJkZUQAAAABXSBlRAAAAAAA=",
      "xid": "G2Q6OcsXq1k0pA0mMNHVH1P02Tw=",
      "transactionId": "f38e6948-5388-41a6-bca4-b49723c19437",
      "authenticationResponse": "Y",
      "transactionStatus": "Y"
  }
}
```  

  


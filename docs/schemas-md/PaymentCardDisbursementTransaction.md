
# PaymentCardDisbursementTransaction

| *description*:   | *Request to create disbursement transaction using a payment card.*|
|----|----|
| requestType |    ``` string ```  *example:   PaymentCardCreditTransaction*.Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  TransactionOrigin  ``` string ```  *example: ECOM*.The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ``` ($int64)  *example: 838916029301*. The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  *example: true*. Indicates if the particular transaction is a partial approval transaction, if supplied.|
| disbursement | [Disbursement](?path=docs/schemas-md/Disbursement.md)|
| paymentMethod | [PaymentCardPaymentMethod](?path=docs/schemas-md/PaymentCardPaymentMethod.md)|
| storedCredentials | [StoredCredential](?path=docs/schemas-md/StoredCredential.md)|
| createToken | [CreatePaymentToken](?path=docs/schemas-md/CreatePaymentToken.md)|    

**PaymentCardDisbursementTransaction Example:**
```{r}
{
  "requestType": "PaymentCardDisbursementTransaction",
  "transactionAmount": {
    "total": "50",
    "currency": "USD"
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
  },
  "paymentMethod": {
    "paymentCard": {
      "number": "5424180279791732",
      "expiryDate": {
        "month": "12",
        "year": "25"
      },
      "securityCode": "977"
    }
  }
}   
```  







   



 
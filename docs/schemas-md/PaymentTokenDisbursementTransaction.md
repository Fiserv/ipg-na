
# PaymentTokenDisbursementTransaction

| *description*:   | *Request to create disbursement transaction using a payment token.*|
|----|----|
| requestType |    ``` string ```   <br/> *example:   PaymentCardCreditTransaction*  <br/> Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```   <br/> maxLength: 20   <br/> *example: 12345500000*.  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   <br/> maxLength: 40  <br/> *example: lsk23532djljff3*.  <br/> The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md)  <br/>  ``` string ```   <br/> *example: ECOM*. <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face).  <br/> Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ```  <br/> ($int64)   <br/> *example: 838916029301*.  <br/> The response transaction ID.|
| allowPartialApproval |    ``` boolean ```   <br/> *example: true*.  <br/> Indicates if the particular transaction is a partial approval transaction, if supplied.|
| disbursement | [Disbursement](?path=docs/schemas-md/Disbursement.md)|
| paymentMethod | [PaymentTokenPaymentMethod](?path=docs/schemas-md/PaymentTokenPaymentMethod.md)|
| storedCredentials | [StoredCredential](?path=docs/schemas-md/StoredCredential.md)|   

**PaymentTokenDisbursementTransaction Example:**

```{r}

{
  "requestType": "PaymentTokenDisbursementTransaction",
  "transactionAmount": {
    "total": "50",
    "currency": "USD"
  },
  "disbursement": {
    "disbursementType": "DisbursementTransactionType",
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
    "paymentToken": {
      "value": "1235325235236",
      "function": "DEBIT",
      "securityCode": "977"
    }
  }
}
```  

   







   



 


# PaymentCardForcedTicketTransaction

| *description*:   | *Request to create forced ticket primary transaction.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentCardCreditTransaction*  <br/> Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ``` <br/> maxLength: 20  *example: 12345500000*  <br/>  An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   <br/> maxLength: 40  <br/> *example: lsk23532djljff3*  <br/> The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md)  <br/>  ``` string ```  <br/>  *example: ECOM*  <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). <br/>  Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ```  <br/> ($int64)  <br/>  *example: 838916029301*  <br/> The response transaction ID.|
| allowPartialApproval |    ``` boolean ``` <br/>   *example: true* <br/>  Indicates if the particular transaction is a partial approval transaction, if supplied.|
| paymentMethod | [PaymentCardPaymentMethod](?path=docs/schemas-md/PaymentCardPaymentMethod.md)|
| referenceNumber |    ``` string ```  <br/> maxLength: 8  pattern: ^(?!\s*$).+   <br/> *example: 123455*  <br/> Stores the six-digit reference number you have received as the result of a successful external authorization (e.g. by phone). The gateway needs this number for uniquely mapping a ForcedTicket transaction to a previously performed external authorization.|   

*PaymentCardForcedTicketTransaction Example:**

```{r}

{
  "transactionAmount": {
    "total": 12.04,
    "currency": "USD"
  },
  "requestType": "PaymentCardForcedTicketTransaction",
  "paymentMethod": {
    "paymentCard": {
      "number": "5424180279791732",
      "securityCode": "977",
      "expiryDate": {
        "month": "12",
        "year": "24"
      }
    }
  },
  "referenceNumber": "123455"
}
```


# SepaCreditTransaction

| *description*:   | *Request to create credit transaction using sepa.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example:   PaymentCardCreditTransaction* <br/> Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  <br/> maxLength: 20   <br/> *example: 12345500000* <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   <br/>  maxLength: 40  <br/> *example: lsk23532djljff3* <br/> The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md)  <br/>  ``` string ```  <br/>  *example: ECOM*  <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ```  <br/> ($int64)  <br/>  *example: 838916029301* <br/>  The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  <br/>  *example: true* <br/>  Indicates if the particular transaction is a partial approval transaction, if supplied.|
| paymentMethod | [SepaCreditPaymentMethod](?path=docs/schemas-md/SepaCreditPaymentMethod.md)|   

**SepaCreditTransaction Example:**

```{r}

{
  "transactionAmount": {
    "total": "23.00",
    "currency": "EUR"
  },
  "requestType": "SepaCreditTransaction",
  "sepa": {
    "iban": "DE34500100600032121604",
    "name": "John Doe"
  },
  "order": {
    "billing": {
      "address": {
        "address1": "102,1st Floor",
        "address2": "123 Main St.",
        "postalCode": "30303",
        "city": "Sandy Springs",
        "country": "DEU"
      }
    }
  }
}
```

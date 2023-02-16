
# ApmPreAuthTransaction

| *description*:   | *Request to create preAuth transaction using an alternative payment method (see methods supported by this transaction type below).*|
|----|----|
| requestType |    ``` string ```   <br/> *example:   PaymentCardCreditTransaction*. <br/> Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  <br/> maxLength: 20   <br/> *example: 12345500000*. <br/>  An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   <br/> maxLength: 40  <br/> *example: lsk23532djljff3*.  <br/> The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md)  <br/>  ``` string ```  <br/>  *example: ECOM*. <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ``` <br/>  ($int64)  <br/>  *example: 838916029301*. <br/>  The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  <br/>  *example: true*.  <br/> Indicates if the particular transaction is a partial approval transaction, if supplied.|
| paymentMethod |  [ApmPaymentMethod](?path=docs/schemas-md/ApmPaymentMethod.md)|
| integrationData | [Integration data to provide information from the application. [IntegrationData](?path=docs/schemas-md/IntegrationData.md)]|
| consumerData | [Integration data provided by the payer. [ConsumerData](?path=docs/schemas-md/ConsumerData.md)]|   


**ApmPreAuthTransaction Example:**

```{r}

{
  "transactionAmount": {
    "total": "40.00",
    "currency": "PLN"
  },
  "requestType": "ApmPreAuthTransaction",
  "paymentMethod": {
    "type": "BLIK"
  },
  "integrationData": [
    {
      "item": "RETURN_URL",
      "value": "https://clientdomain.com/orderDetails"
    },
    {
      "item": "PAYER_IP",
      "value": "1.1.1.1"
    }
  ],
  "consumerData": [
    {
      "item": "BLIK_CODE",
      "value": "777153"
    }
  ]
}
```

   



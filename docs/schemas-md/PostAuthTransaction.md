
# PostAuthTransaction

| *description*:   | *Request to perform post auth transaction.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PostAuthTransaction* <br/> Object name of the primary transaction request.|
| storeId |    ``` string ```  <br/> maxLength: 20  <br/> *example: 12345500000* <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   <br/> maxLength: 40  <br/> *example: lsk23532djljff3* <br/> The unique merchant transaction ID from the request, if supplied.|
| comments |    ``` string ```  <br/> maxLength: 1024   <br/> *example: This is a comment* <br/> Comments for the payment.|
| order | [Order](?path=docs/schemas-md/Order.md)|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| transactionOrigin |  [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md)  <br/>  ``` string ```  <br/>  *example: ECOM*  <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| splitShipment | [SplitShipment](?path=docs/schemas-md/SplitShipment.md)|
| softDescriptor | [SoftDescriptor](?path=docs/schemas-md/SoftDescriptor.md)|
| parDataRequested |    ``` boolean ```  <br/> default: false  <br/> *example: false* <br/> Indicates if the merchant wants payment account reference number from the network token using endpoint(PaymentAccountReferenceFlag = true).|

**PostAuthTransaction Example:**

```{r}

{
  "requestType": "PostAuthTransaction",
  "transactionAmount": {
    "total": 12.04,
    "currency": "USD"
  },
  "splitShipment": {
    "totalCount": 1,
    "finalShipment": true
  }
}
```   





   



 

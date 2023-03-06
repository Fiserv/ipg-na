
# ReturnTransaction

| *description*:   | *Request to perform return transaction.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PostAuthTransaction* <br/> Object name of the primary transaction request.|
| storeId |    ``` string ```   <br/> maxLength: 20  <br/> *example: 12345500000* <br/>  An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```  <br/> maxLength: 40  <br/> *example: lsk23532djljff3* <br/>  The unique merchant transaction ID from the request, if supplied.|
| comments |    ``` string ```  <br/> maxLength: 1024  <br/> *example: This is a comment*  <br/>  Comments for the payment.|
| order | [Order](?path=docs/schemas-md/Order.md)|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| softDescriptor | [SoftDescriptor](?path=docs/schemas-md/SoftDescriptor.md)|
| storedCredentials | [StoredCredential](?path=docs/schemas-md/StoredCredential.md)|
| currencyConversion | [CurrencyConversion](?path=docs/schemas-md/CurrencyConversion.md)|

**ReturnTransaction Example:**

```{r}

{
  "requestType": "ReturnTransaction",
  "transactionAmount": {
    "total": 12.04,
    "currency": "USD"
  },
  "currencyConversion": {
    "conversionType": "Dcc",
    "inquiryRateId": "123456"
  }
}
```   





   



 

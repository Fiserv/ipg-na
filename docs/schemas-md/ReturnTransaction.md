
# ReturnTransaction

| *description*:   | *Request to perform return transaction.*|
|----|----|
| requestType |    ``` string ```  *example:   PostAuthTransaction*.Object name of the primary transaction request.|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| comments |    ``` string ```  *maxLength: 1024   example: This is a comment.*  Comments for the payment.|
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





   



 

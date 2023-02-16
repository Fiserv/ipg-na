
# AchPostAuthTransaction

| *description*:   | *Request to perform ACH telecheck post auth transaction.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example:   PostAuthTransaction*.  <br/> Object name of the primary transaction request.|
| storeId |    ``` string ```   <br/> maxLength: 20  <br/>  *example: 12345500000*.  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   maxLength: 40  <br/>  *example: lsk23532djljff3*.  <br/> The unique merchant transaction ID from the request, if supplied.|
| comments |    ``` string ```   <br/> maxLength: 1024    <br/> *example: This is a comment.*   <br/> Comments for the payment.|
| order | [Order](?path=docs/schemas-md/Order.md)|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|

**AchPostAuthTransaction Example:**

```{r}

{
  "requestType": "AchPostAuthTransaction",
  "transactionAmount": {
    "total": 12.04,
    "currency": "USD"
  }
}
```   






   



 

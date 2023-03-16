
# VoidTransaction

| *description*:   | *Request to perform void transaction.*|
|----|----|
| requestType |    ``` string ```   <br/> *example: VoidTransaction* <br/> Object name of the primary transaction request.|
| storeId |    ``` string ```  <br/>  maxLength: 20   <br/> *example: 12345500000* <br/>  An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```  <br/>   maxLength: 40 *example: lsk23532djljff3* <br/>  The unique merchant transaction ID from the request, if supplied.|
| comments |    ``` string ```  <br/>  maxLength: 1024   <br/> *example: This is a comment.*  <br/>  Comments for the payment.|
| order | [Order](?path=docs/schemas-md/Order.md)|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|

**VoidTransaction Example:**

```{r}

{
  "requestType": "VoidTransaction",
  "comments": "This is a comment"
}
```   





   



 

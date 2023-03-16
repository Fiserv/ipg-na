
# VoidPreAuthTransactions

| *description*:   | *Request to perform a void of all authorizations associated with the current order. This request type is applicable for voiding preauth and incremental preauth transactions.*|
|----|----|
| requestType |    ``` string ``` <br/> *example: PostAuthTransaction.*  <br/> Object name of the primary transaction request.|
| storeId |    ``` string ```  <br/>  maxLength: 20 <br/>   *example: 12345500000*.  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```  <br/>   * maxLength: 40  <br/> example: lsk23532djljff3*.  <br/> The unique merchant transaction ID from the request, if supplied.|
| comments |    ``` string ```  <br/>  maxLength: 1024  <br/>  *example: This is a comment.*  <br/>  Comments for the payment.|
| order | [Order](?path=docs/schemas-md/Order.md)|

**VoidPreAuthTransactions Example:**

```{r}

{
  "requestType": "VoidPreAuthTransactions",
  "comments": "This is a comment"
}
```   





   



 

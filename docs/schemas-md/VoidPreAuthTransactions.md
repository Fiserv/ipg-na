
# VoidPreAuthTransactions

| *description*:   | *Request to perform a void of all authorizations associated with the current order. This request type is applicable for voiding preauth and incremental preauth transactions.*|
|----|----|
| requestType |    ``` string ```  *example:   PostAuthTransaction.* Object name of the primary transaction request.|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| comments |    ``` string ```  *maxLength: 1024   example: This is a comment.*  Comments for the payment.|
| order | [Order](?path=docs/schemas-md/Order.md)|

**VoidPreAuthTransactions Example:**

```{r}

{
  "requestType": "VoidPreAuthTransactions",
  "comments": "This is a comment"
}
```   





   



 

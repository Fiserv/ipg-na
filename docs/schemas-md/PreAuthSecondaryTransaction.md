
# PreAuthSecondaryTransaction

| *description*:   | *Request to perform pre-auth incremental secondary transaction without providing credit card information.*|
|----|----|
| requestType |    ``` string ```  *example:   PaymentCardCreditTransaction*.Object name of the primary transaction request.|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| comments |    ``` string ```  *maxLength: 1024   example: This is a comment.*  Comments for the payment.|
| order | [Order](?path=docs/schemas-md/Order.md)|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| decrementalFlag |  DecrementalPreAuthFlag  ``` boolean ```  *default: false  example: false*. This flag can only be used in a preAuth transaction that updates the amount of a previous preAuth transaction to either increase the preAuth amount (DecrementalPreAuthFlag = false) or decrease the preAuth amount (DecrementalPreAuthFlag = true).|
| incrementalFlag |  IncrementalPreAuthFlag  ``` boolean ```  *default: false example: false*. This flag can only be used in a preAuth transaction that updates the amount of a previous preAuth transaction to increase the preAuth amount (IncrementalPreAuthFlag = true).|

**PreAuthSecondaryTransaction Example:**

```{r}

{
  "requestType": "PreAuthSecondaryTransaction",
  "transactionAmount": {
    "total": "5.00",
    "currency": "USD"
  },
  "decrementalFlag": false,
  "incrementalFlag": false
}
```   

   



 

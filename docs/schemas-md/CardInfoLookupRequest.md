
# CardInfoLookupRequest

| *description*:   | *Request to look up card-related information such as issuer country, card function and card brand.*|
|----|----|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| paymentCard* | [PaymentCard](?path=docs/schemas-md/PaymentCard.md)|


**CardInfoLookupRequest Example:**

```{r}

{
  "paymentCard": {
    "number": "4149011500000147"
  }
}
```  
  


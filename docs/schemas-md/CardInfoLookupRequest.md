
# CardInfoLookupRequest

| *description*:   | *Request to look up card-related information such as issuer country, card function and card brand.*|
|----|----|
| storeId |    ``` string ```  <br/>  maxLength: 20   <br/> *example: 12345500000*.  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| paymentCard* | [PaymentCard](?path=docs/schemas-md/PaymentCard.md)|


**CardInfoLookupRequest Example:**

```{r}

{
  "paymentCard": {
    "number": "4149011500000147"
  }
}
```  
  


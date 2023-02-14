
# PaymentCardInfoLookupRequest

| *description*:   | *Used to request information associated with a payment card.*|
|----|----|
| requestType |    ``` string ```  *example: PaymentCardInfoLookupRequest* Object name of the account verification request.|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| paymentCard* | [PaymentCard](?path=docs/schemas-md/PaymentCard.md)|


**PaymentCardInfoLookupRequest Example:**

```{r}

{
    "requestType": "PaymentCardInfoLookupRequest",
    "paymentCard": OrderedMap {
        "number": "4149011500000147"
    }
}
```  
  


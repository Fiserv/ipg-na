
# PaymentCardInfoLookupRequest

| *description*:   | *Used to request information associated with a payment card.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentCardInfoLookupRequest* <br/>  Object name of the account verification request.|
| storeId |    ``` string ``` <br/> maxLength: 20  <br/> *example: 12345500000*  <br/>  An optional outlet ID for clients that support multiple stores in the same app.|
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
  



# AccountInfoLookupRequest

| *description*:   | *Request to look up card-related information such as issuer country, card function and card brand associated with a payment card or payment token.  <br/> Abstract class, do not use this class directly, use one of its children.*|
|----|----|
| requestType |    ``` string ```   <br/> *example: PaymentCardInfoLookupRequest* <br/>  Object name of the account verification request.|
| storeId |    ``` string ```  <br/>  *maxLength: 20  example: 12345500000*.  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| paymentCard* | [PaymentCard](?path=docs/schemas-md/PaymentCard.md)|


**AccountInfoLookupRequest Example:**

```{r}

{
    "requestType": "PaymentCardInfoLookupRequest",
    "paymentCard": OrderedMap {
        "number": "4149011500000147"
    }
}
```  
  


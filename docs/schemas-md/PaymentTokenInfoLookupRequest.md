
# PaymentTokenInfoLookupRequest

| *description*:   | *Used to request card information associated with a payment token.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentCardInfoLookupRequest* Object name of the account verification request.|
| storeId |    ``` string ```   <br/> maxLength: 20   <br/> *example: 12345500000*.  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| paymentToken* | [UsePaymentToken](?path=docs/schemas-md/UsePaymentToken.md)|


**PaymentTokenInfoLookupRequest Example:**

```{r}

{
    "value": "1235325235236",
    "tokenOriginStoreId": "12345500001",
    "function": "DEBIT",
    "securityCode": "977",
    "expiryDate": OrderedMap {
        "month": "12",
        "year": "24"
    }
}
```  
  


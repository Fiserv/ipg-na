
# ChinaPnRSaleTransaction

| *description*:   | *Request to create sale transaction using China PnR.*|
|----|----|
| requestType |    ``` string ```   <br/> *example:   PaymentCardCreditTransaction*   <br/> Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  <br/> maxLength: 20   <br/> *example: 12345500000*.  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   <br/>  maxLength: 40  <br/> *example: lsk23532djljff3*.  <br/> The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md)  <br/>   ``` string ```  <br/> *example: ECOM*. <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). <br/>  Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ```  <br/> ($int64)  <br/>  *example: 838916029301*.  <br/> The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  <br/>  *example: true*. <br/>  Indicates if the particular transaction is a partial approval transaction, if supplied.|
| paymentMethod |  [ChinaDomesticPaymentMethod](?path=docs/schemas-md/ChinaDomesticPaymentMethod.md)|    

**ChinaPnRSaleTransaction Example:**

```{r}

{
  "transactionAmount": {
    "total": "40.00",
    "currency": "CNY"
  },
  "requestType": "ChinaPnRSaleTransaction",
  "paymentMethod": {
    "chinaDomestic": {
      "productCode": "R2D2C3PO",
      "productQuantity": 10,
      "productPrice": 3.2,
      "productDescription": "Best product ever",
      "redirectURL": "www.urlredirectedto.com"
    },
    "brand": "WECHAT_DOMESTIC"
  }
}
```



   




# ChinaPnRSaleTransaction

| *description*:   | *Request to create sale transaction using China PnR.*|
|----|----|
| requestType |    ``` string ```  *example:   PaymentCardCreditTransaction*.Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  TransactionOrigin  ``` string ```  *example: ECOM*.The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ``` ($int64)  *example: 838916029301*. The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  *example: true*. Indicates if the particular transaction is a partial approval transaction, if supplied.|
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



   




# KoreanPaymentSaleTransaction

| *description*:   | *Request to create sale transaction for Korean Payment.*|
|----|----|
| requestType |    ``` string ```  *example:   PaymentCardCreditTransaction*.Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md) <br/>   ``` string ``` <br/>   *example: ECOM*  <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ``` ($int64)  *example: 838916029301*. The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  *example: true*. Indicates if the particular transaction is a partial approval transaction, if supplied.|
| paymentMethod | [KoreanPaymentMethod](?path=docs/schemas-md/KoreanPaymentMethod.md)|

**KoreanPaymentSaleTransaction Example:**

```{r}

{
  "transactionAmount": {
    "total": "4000",
    "currency": "KRW"
  },
  "requestType": "KoreanPaymentSaleTransaction",
  "paymentMethod": {
    "koreanPayment": {
      "billKeyId": "testipg5000000",
      "entry": "web",
      "billType": "TAX_FREE"
    }
  }
}
```  


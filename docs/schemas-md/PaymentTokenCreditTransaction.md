
# PaymentTokenCreditTransaction

| *description*:   | *Request to create credit transaction using payment token.*|
|----|----|
| requestType |    ``` string ```  *example:   PaymentCardCreditTransaction*.Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  TransactionOrigin  ``` string ```  *example: ECOM*.The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ``` ($int64)  *example: 838916029301*. The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  *example: true*. Indicates if the particular transaction is a partial approval transaction, if supplied.|
| paymentMethod | [PaymentTokenPaymentMethod](?path=docs/schemas-md/PaymentTokenPaymentMethod.md)|   
| currencyConversion | [CurrencyConversion](?path=docs/schemas-md/CurrencyConversion.md)|   
 

   



 

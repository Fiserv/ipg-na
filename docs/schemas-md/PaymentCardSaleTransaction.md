
# PaymentCardSaleTransaction

| *description*:   | *Request to create sale transaction using payment card.*|
|----|----|
| requestType |    ``` string ```  *example:   PaymentCardCreditTransaction*.Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  TransactionOrigin  ``` string ```  *example: ECOM*.The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ``` ($int64)  *example: 838916029301*. The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  *example: true*. Indicates if the particular transaction is a partial approval transaction, if supplied.|
| paymentMethod | [PaymentCardPaymentMethod](?path=docs/schemas-md/PaymentCardPaymentMethod.md)|
| storedCredentials | [StoredCredential](?path=docs/schemas-md/StoredCredential.md)|
| settlementSplit | [SettlementSplit](?path=docs/schemas-md/SettlementSplit.md)|
| createToken | [CreatePaymentToken](?path=docs/schemas-md/CreatePaymentToken.md)|
| currencyConversion | [CurrencyConversion](?path=docs/schemas-md/CurrencyConversion.md)|
| authenticationRequest | [AuthenticationRequest](?path=docs/schemas-md/AuthenticationRequest.md)| 
| authenticationResult | [AuthenticationResult](?path=docs/schemas-md/AuthenticationResult.md)|
| decrementalFlag |  DecrementalPreAuthFlag  ``` boolean ```  *default: false  example: false*. This flag can only be used in a preAuth transaction that updates the amount of a previous preAuth transaction to either increase the preAuth amount (DecrementalPreAuthFlag = false) or decrease the preAuth amount (DecrementalPreAuthFlag = true).|
| parDataRequested |  PaymentAccountReferenceFlag  ``` boolean ```  *default: false example: false*. Indicates if the merchant wants payment account reference number from the network token using endpoint(PaymentAccountReferenceFlag = true).|    





   



 


# PaymentCardSaleTransaction

| *description*:   | *Request to create sale transaction using payment card.*|
|----|----|
| requestType |    ``` string ``` <br/>   *example: PaymentCardCreditTransaction*  <br/> Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  <br/> maxLength: 20  <br/> *example: 12345500000*  <br/>  An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```  <br/> maxLength: 40  <br/> *example: lsk23532djljff3*  <br/>  The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md)  <br/>  ``` string ```  <br/>  *example: ECOM*  <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ```  <br/> ($int64)  <br/>  *example: 838916029301*  <br/>  The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  <br/>  *example: true*  <br/>  Indicates if the particular transaction is a partial approval transaction, if supplied.|
| paymentMethod | [PaymentCardPaymentMethod](?path=docs/schemas-md/PaymentCardPaymentMethod.md)|
| storedCredentials | [StoredCredential](?path=docs/schemas-md/StoredCredential.md)|
| settlementSplit | [SettlementSplit](?path=docs/schemas-md/SettlementSplit.md)|
| createToken | [CreatePaymentToken](?path=docs/schemas-md/CreatePaymentToken.md)|
| currencyConversion | [CurrencyConversion](?path=docs/schemas-md/CurrencyConversion.md)|
| authenticationRequest | [AuthenticationRequest](?path=docs/schemas-md/AuthenticationRequest.md)| 
| authenticationResult | [AuthenticationResult](?path=docs/schemas-md/AuthenticationResult.md)|
| decrementalFlag |  DecrementalPreAuthFlag  ``` boolean ```  <br/> default: false  <br/> *example: false*  <br/> This flag can only be used in a preAuth transaction that updates the amount of a previous preAuth transaction to either increase the preAuth amount (DecrementalPreAuthFlag = false) or decrease the preAuth amount (DecrementalPreAuthFlag = true).|
| parDataRequested |   [PaymentAccountReferenceFlag](?path=docs/schemas-md/PaymentAccountReferenceFlag.md)  <br/>  ``` boolean ```  <br/> default: false  <br/> *example: false* <br/> Indicates if the merchant wants payment account reference number from the network token using endpoint(PaymentAccountReferenceFlag = true).|    

**PaymentCardSaleTransaction Example:**

```{r}

{
  "transactionAmount": {
    "total": 12.04,
    "currency": "USD"
  },
  "requestType": "PaymentCardSaleTransaction",
  "paymentMethod": {
    "paymentCard": {
      "number": "5424180279791732",
      "securityCode": "977",
      "expiryDate": {
        "month": "12",
        "year": "24"
      }
    }
  },
  "storedCredentials": {
    "sequence": "FIRST",
    "scheduled": true
  },
  "authOptimizationOverride": "Override"
}
```  




   



 

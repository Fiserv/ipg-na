
# WalletPreAuthTransaction

| *description*:   | *Request to create preAuth primary transaction using digital wallet.*|
|----|----|
| requestType |    ``` string ```   <br/> *example: PaymentCardCreditTransaction* <br/> Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ``` <br/>   *maxLength: 20   <br/> example: 12345500000* <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```  <br/>   maxLength: 40  <br/> *example: lsk23532djljff3* <br/>  The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md)  <br/>  ``` string ```  <br/>  *example: ECOM*. <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face).  <br/> Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ```  <br/>  ($int64)  <br/>  *example: 838916029301* <br/>  The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  <br/>  *example: true* <br/> Indicates if the particular transaction is a partial approval transaction, if supplied.|
| walletPaymentMethod | [WalletPaymentMethod](?path=docs/schemas-md/WalletPaymentMethod.md)|   
| authenticationRequest | [AuthenticationRequest](?path=docs/schemas-md/AuthenticationRequest.md)| 
| authenticationResult | [AuthenticationResult](?path=docs/schemas-md/AuthenticationResult.md)|
| splitShipment | [SplitShipment](?path=docs/schemas-md/SplitShipment.md)|  
| paymentFacilitator | [PaymentFacilitator](?path=docs/schemas-md/PaymentFacilitator.md)|     
| decrementalFlag |  DecrementalPreAuthFlag  ``` boolean ```  <br/>  *default: false  example: false* <br/>  This flag can only be used in a preAuth transaction that updates the amount of a previous preAuth transaction to either increase the preAuth amount (DecrementalPreAuthFlag = false) or decrease the preAuth amount (DecrementalPreAuthFlag = true).|
| incrementalFlag |  IncrementalPreAuthFlag  ``` boolean ```   <br/> *default: false example: false* <br/> This flag can only be used in a preAuth transaction that updates the amount of a previous preAuth transaction to increase the preAuth amount (IncrementalPreAuthFlag = true).|   

**WalletPreAuthTransaction Example:**

```{r}

{
  "requestType": "WalletPreAuthTransaction",
  "walletPaymentMethod": {
    "walletType": "EncryptedGooglePayWalletPaymentMethod",
    "encryptedGooglePay": {
      "data": {
        "encryptedMessage": "8nxjB9mr2tWZeDRQRcGN91UUnb7AioGp3oRo8kmQ6lyvJZiqD7PJlbRCYElNqUmr6Z8zK7b2gO9MKOjpnTCqH0qAe2vuIlwNXB60M2Lh7Qfl3bVgWzwF/FfFcenVW381hoItYi8AjWnWoydz1XMTEv2qhqUG03mEnRXdMyDyk6KKZXoW8Qc0p1F1thbxxu8weU8CZbZsWGGTjB42cilIqLVbribcOAG8Oas1AcgefFsu2hwp4gdSuOg7wmeSV7XKsGQzzVy85qtjuqET2XYzJE3K/Wh9QKkhu5P9Ms5s1+Smr2IjRyidqQa88SxQplrVoo9+PvT0bxFcMspBmO3pLkuaZSUBy++dL2fefcxNJvGCFfFhdxW9DojuuQxgpeu7RAQUsGLyFmr/4ZfBxt882xTmpX9MRx5CAudl9qUgBfKdwWwMX35qSbDTm1ju5XXzNh94VebjD3bB9Zj8qgbmUOr/+6OQLhoFJyBCXgx3EEH8hBwNVFrss/SLwQvFhZh62eO6lOtnmbOtP1yTDDVqGDBfai5SwAmM+KTcc9SGv/xDC+cWe8ck+aCBkG4HoRPapUVMZ3JIgV7yzTsVLJE\\\\u003d\\\\",
        "ephemeralPublicKey": "BGH3fRFdoAobYrAlxnZOCYzkH84Cna92IZxtgsU36CMDaqSaDYb9/LsY8qw+vMtlBnwsUg/YVMOeeKp+qDkOWb4\\\\u003d\\\\",
        "tag": "nvmOUNpnOTZULLhMxT/hWCHzH/4f7gGpfvQgwl3p8ng\\\\u003d\\\\"
      },
      "signature": "MEUCIFWTRWUZAOM5nfJC79FtJm56olnbwG4H5uWWxAUWAquiAiEA24j/BcOroeISsdJzYsyoVi8wzu4tnmKw+jdsGfuvPko=",
      "version": "ECv1"
    }
  },
  "splitShipment": {
    "totalCount": 1,
    "finalShipment": true
  }
}   
```

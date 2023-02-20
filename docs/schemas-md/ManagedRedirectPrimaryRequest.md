
# ManagedRedirectPrimaryRequest

| *description*:   | *Request to generate an embedded payment link for Managed redirect.*|
|----|----|
| requestType* |    ``` string ```   <br/>  *example: PaymentCardManagedRedirectRequest* <br/> Object name of the primary transaction request.|
| transactionAmount* | [Amount](?path=docs/schemas-md/Amount.md)|  
| storeId | [TokenCryptogram](?path=docs/schemas-md/TokenCryptogram.md)  <br/>   ``` string ```  <br/>  maxLength: 20 <br/> *example: 12345500000* <br/> An optional Outlet ID for clients that support multiple stores in the same developer app.|
| merchantTransactionId |    ``` string ``` <br/> maxLength: 40 <br/> *example: lsk23532djljff3* <br/> The unique merchant transaction ID from the request, if supplied.|
| transactionType |  [ManagedRedirectTransactionType](?path=docs/schemas-md/ManagedRedirectTransactionType.md)  <br/> ``` string ```   *example: SALE* <br/> Type of transaction to perform with ManagedRedirectPrimaryRequest. Primary transaction types in requests include 'SALE', 'PREAUTH', 'PAYER_AUTH'. <br/> Enum:[ SALE, PREAUTH, PAYER_AUTH ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| redirectAttributes | [RedirectAttributes](?path=docs/schemas-md/RedirectAttributes.md)|   



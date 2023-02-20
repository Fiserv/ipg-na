
# KoreanPaymentServiceReturnTransaction

| *description*:   | *Request to perform Korean Payment Service return transaction.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentCardCreditTransaction*  <br/> Object name of the primary transaction request.|
| storeId |    ``` string ```   <br/> maxLength: 20   <br/> *example: 12345500000*.  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   <br/>  maxLength: 40  <br/> *example: lsk23532djljff3*.  <br/> The unique merchant transaction ID from the request, if supplied.|
| comments |    ``` string ```  <br/> maxLength: 1024    <br/> *example: This is a comment.*  <br/>  Comments for the payment.|
| order | [Order](?path=docs/schemas-md/Order.md)|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| returnAccountNumber |   ``` string ```  <br/>  *maxLength: 16*|
| returnBankCode |   ``` string ```  <br/>  *maxLength: 3*|
| returnAccountHolderName |   ``` string ```  <br/>  *maxLength: 20*|
| returnReason |   ``` string ``` <br/>   *maxLength: 256*|   







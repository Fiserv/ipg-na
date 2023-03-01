
# PaymentTokenVerificationRequest

| *description*:   | *Used to request account verification using a payment token.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentCardVerificationRequest* <br/> Object name of the account verification request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|  
| storeId |    ``` string ```  <br/> maxLength: 20  <br/> *example: 12345500000* <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   <br/> maxLength: 40  <br/> *example: lsk23532djljff3* <br/> The unique merchant transaction ID from the request, if supplied.|
| additionalDetails | [AdditionalDetails](?path=docs/schemas-md/AdditionalDetails.md)|
| paymentToken | [UsePaymentToken](?path=docs/schemas-md/UsePaymentToken.md)|   

    
   




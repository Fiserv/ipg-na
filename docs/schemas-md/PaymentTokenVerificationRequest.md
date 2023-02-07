
# PaymentTokenVerificationRequest

| *description*:   | *Used to request account verification using a payment token.*|
|----|----|
| requestType |    ``` string ```  *example: PaymentCardVerificationRequest*. Object name of the account verification request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|  
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| additionalDetails | [AdditionalDetails](?path=docs/schemas-md/AdditionalDetails.md)|
| paymentToken | [UsePaymentToken](?path=docs/schemas-md/UsePaymentToken.md)|   

    
   




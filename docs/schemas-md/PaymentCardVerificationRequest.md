
# PaymentCardVerificationRequest

| *description*:   | *Used to request account verification using a payment card. The expiryDate in paymentCard object is required to perform a PaymentCardVerificationRequest.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentCardVerificationRequest*  <br/> Object name of the payment schedules request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|  
| storeId |    ``` string ```  <br/>  *maxLength: 20   <br/> example: 12345500000*  <br/>  An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```  <br/> *maxLength:  <br/> 40 example: lsk23532djljff3*  <br/> The unique merchant transaction ID from the request, if supplied.|
| additionalDetails | [AdditionalDetails](?path=docs/schemas-md/AdditionalDetails.md)|
| paymentCard | [PaymentCard](?path=docs/schemas-md/PaymentCard.md)|  


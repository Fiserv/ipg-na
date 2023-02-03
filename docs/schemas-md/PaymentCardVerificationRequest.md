
# PaymentCardVerificationRequest

| *description*:   | *Used to request account verification using a payment card. The expiryDate in paymentCard object is required to perform a PaymentCardVerificationRequest.*|
|----|----|
| requestType |    ``` string ```  *example:   PaymentCardVerificationRequest*. Object name of the payment schedules request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|  
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| additionalDetails | [AdditionalDetails](?path=docs/schemas-md/AdditionalDetails.md)|
| paymentCard | [PaymentCard](?path=docs/schemas-md/PaymentCard.md)|  


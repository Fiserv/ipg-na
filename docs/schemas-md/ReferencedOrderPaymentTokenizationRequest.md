
# ReferencedOrderPaymentTokenizationRequest

| *description*:   | *Used to generate payment tokens with an existing order ID.*|
|----|----|
| requestType |    ``` string ```  *example: PaymentCardVerificationRequest*. Object name of the account verification request.|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| billingAddress |    |  
| createToken |   |     
| accountVerification |  ``` boolean ```  *default: false  example: true*. If the account should be verified prior to token creation.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| additionalDetails |    |
| referencedOrderId |  ``` string ```  *pattern: ^(?!\s*$).+  example: R-f9c2c198-b7cc-491a-a711-93d22fd0e589* Order ID used to create recurring payment from existing transaction.|  






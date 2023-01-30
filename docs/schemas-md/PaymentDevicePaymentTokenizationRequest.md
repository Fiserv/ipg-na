
# PaymentDevicePaymentTokenizationRequest

| *description*:   | *Used to generate payment tokens during payment using a payment device.*|
|----|----|
| requestType |    ``` string ```  *example: PaymentDevicePaymentTokenizationRequest*. Object name of the payment schedules request.|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| billingAddress |    |
| createToken |    |
| accountVerification |  ``` boolean ```  *default: false  example: true*. If the account should be verified prior to token creation.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| additionalDetails |    |
| paymentDevice |    |   







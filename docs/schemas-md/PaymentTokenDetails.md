
# PaymentTokenDetails

| *description*:   | *Response details for payment token creation.*|
|----|----|
| value |    ``` string ```  *example:  234ljl124l12*. Client-supplied payment token value. Only applicable for DataVault tokenization scheme.|
| reusable |    ``` boolean ```  *default: true  example: true*. If the token is reusable.|
| declineDuplicates |    ``` boolean ```  *default: false  example: false*. Decline duplicate payment info if client token is supplied.|
| last4 |    ``` string ```  *example: 4997*. The last 4 numbers of a payment card.|
| brand |    ``` string ```  *example: VISA*. Card brand, only for tokenization with payment.|
| accountVerification |    ``` boolean ```  *example: true*. If the account the token was created from has been verified.|
| type |    ``` string ```  *example: PAYMENT_CARD*. Indicates the type of tokenization source.|
| error |     |    



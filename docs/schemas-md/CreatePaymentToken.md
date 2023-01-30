
# CreatePaymentToken

| *description*:   | *Use this model to create a payment token.*|
|----|----|
| value |    ``` string ```  *example:  234ljl124l12*. Client-supplied payment token value. Only applicable for DataVault tokenization scheme.|
| reusable |    ``` boolean ```  *default: true  example: true*. If the token is reusable.|
| declineDuplicates |    ``` boolean ```  *default: false  example: false*. Decline duplicate payment info if client token is supplied.|   
2023-01-30 12:16:34 Monday
| **CreatePaymentToken Example**  | ``` { "value": "234ljl124l12", "reusable": true, "declineDuplicates": false } ``` |  
 




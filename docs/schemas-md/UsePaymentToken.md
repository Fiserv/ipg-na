
# UsePaymentToken

| *description*:   | *Payment token usage details.*|
|----|----|
| value |    ``` string ```  *pattern: ^(?!\s*$).+  example: 1235325235236*. Client-supplied payment token value.|
| tokenOriginStoreId |    ``` string ```  *maxLength: 20  example: 12345500001*. The ID of a same store (or) sibling store in a hierarchy for which the token was originally created.|
| function | CardFunction   ``` string ```  *example: DEBIT*. Card function. This field is required when performing transactions for Brazil merchants. Enum:    > Array [ 5 ] - [ CREDIT, DEBIT, PREPAID, VOUCHER, UNDEFINED ]|
| securityCode |    ``` string ```  *minLength: 3  minLength: 3  example: 977*. Card verification value/number.|
| expiryDate |   |  
| **UpdatePaymentToken Example** | ```  { "value": "3425345345yygg", "reusable": true, "declineDuplicates": false, "paymentCard": {   "number": "5424180279791732", "expiryDate": { "month": "12", "year": "24","securityCode": "977" } } } ``` |    


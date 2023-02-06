
# NetworkToken

| *description*: | *Network Token Model.*|
|----|----|
| value* |  ``` string ```  *string pattern: [0-9]{13,19} example: 2343446334644554.* Token value|
| expiryMonth* | ``` string ```  *pattern: ^(0[1-9]|1[012])$ example: 03.* Month of the token expiration date in MM format.|
| expiryYear* | ``` string ```  *pattern: ^([0-9]{2})$ example: 24.* Year of the card expiration date in YY format.|
| cardLast4 |  ``` string ```  *maxLength: 4 example: 1234.* Last four digits of Card number.|
| brand |  ``` string ```  *example: VISA.* Card brand. Enum:Array [ 8 ] - [ AMEX, DINERS/DISCOVER, EFTPOS, JCB, MAESTRO, MASTERCARD, RUPAY, VISA ]|
| cryptogram |  ``` string ```  *example: AgAAAAADo8FZTI0AmJbMgyUAAAA=* Cryptogram value.|
| authIndicator |  ``` string ```  *example: P. Authorization Indicator. Enum:Array [2] - [ P, T ]|
| tokenEligible |  ``` string ```  *example: AY* Token Assurance Method Value determines the confidence level of the payment token to PAN/cardholder binding and it will be provided by the token service provider.|

**NetworkToken Example:**

```{r}

{
  "number": "5424180279791732",
  "expiryDate": {
    "month": "12",
    "year": "25"
  },
  "securityCode": "977"
}
```  


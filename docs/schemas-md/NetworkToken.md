
# NetworkToken

| *description*: | *Network Token Model.*|
|----|----|
| value* |  ``` string ```  <br/> pattern: [0-9]{13,19}  <br/> *example: 2343446334644554.*  <br/> Token value|
| expiryMonth* | ``` string ```  <br/> pattern: ^(0[1-9]|1[012])$  <br/> *example: 03.*  <br/> Month of the token expiration date in MM format.|
| expiryYear* | ``` string ```   <br/> pattern: ^([0-9]{2})$  <br/> *example: 24.*  <br/> Year of the card expiration date in YY format.|
| cardLast4 |  ``` string ```   <br/> maxLength: 4  <br/> *example: 1234.*  <br/> Last four digits of Card number.|
| brand |  ``` string ```  <br/>  *example: VISA.*  <br/> Card brand.  <br/> Enum:Array [ 8 ] - [ AMEX, DINERS/DISCOVER, EFTPOS, JCB, MAESTRO, MASTERCARD, RUPAY, VISA ]|
| cryptogram |  ``` string ```  <br/>  *example: AgAAAAADo8FZTI0AmJbMgyUAAAA=* <br/>  Cryptogram value.|
| authIndicator |  ``` string ```  <br/>  *example: P*  <br/>  Authorization Indicator.  <br/> Enum:Array [2] - [ P, T ]|
| tokenEligible |  ``` string ```  <br/>  *example: AY*  <br/> Token Assurance Method Value determines the confidence level of the payment token to PAN/cardholder binding and it will be provided by the token service provider.|

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


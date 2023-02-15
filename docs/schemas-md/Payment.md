
# Payment

| *description*: | *Payment information for the transaction.*|
|----|----|
| paymentType* |    ``` string ```  <br/> *example: payment/card* <br/> Defines the type of the payment. <br/>Enum:[ payment/card, payment/wallet ]|
| method* | [Method](?path=docs/schemas-md/Method.md)| 
| pinPresent* |    ``` boolean ```   <br/> *example: true* <br/> Indicates if the cards Personal Identification Number was supplied.|
| entryMethod* |  ``` string ```  <br/> *example: remote* <br/> The method in which the card information entered the system. <br/> Enum:[ manual, stripe, ocr, emv, nfc, remote, pin_present ]|
| issuerResponse | [IssuerResponse](?path=docs/schemas-md/IssuerResponse.md)| 
| issuerApprovedAmount |  ``` string ```  <br/> *example: 1234* <br/> The actual approved amount. This field should be filled in when the message has already passed through the issuer (e.g. post-authorization). For transaction/authorization this amount refers to the amount that was locked on the card-holders account.|
| issuerCardBalance |  ``` string ```  <br/> *example: 2000* <br/>The payment methods account balance if available. This field should be filled in when the message has already passed through the issuer (e.g. post-authorization).|
| verificationAvs | [VerificationAvs](?path=docs/schemas-md/VerificationAvs.md)|
| verification3ds | [Verification3ds](?path=docs/schemas-md/Verification3ds.md)|
| verificationCvv | [VerificationCvv](?path=docs/schemas-md/VerificationCvv.md)|
| userDefined |   {<br/> description: A JSON object that can carry any additional information about the customer that might be helpful for fraud detection. <br/> example:  { "previouslyAffected": "Y" }<br/> }|

**Payment Example:**

```{r}

{
  "paymentType": "payment/card",
  "method": {
    "methodType": "method/card",
    "methodId": "300fa792-bf5f-418e-aa74-d5b3c81298d2",
    "methodAlias": "card one",
    "card": {
      "taToken": "7591787425749818",
      "taTokenKey": "ab56",
      "cardholderName": "John F. Doe",
      "cardNumber": "5424180279791732",
      "expDate": "122028",
      "cvv": "true",
      "issuer": "Bank of America",
      "cardReissuedNumber": "2"
    },
    "provider": "apple"
  },
  "pinPresent": true,
  "entryMethod": "remote",
  "issuerResponse": {
    "code": "100",
    "status": "approved",
    "scheme": "VISA"
  },
  "issuerApprovedAmount": "1234",
  "issuerCardBalance": "2000",
  "verificationAvs": {
    "code": "+Z",
    "status": "zip match",
    "scheme": "amex"
  },
  "verification3ds": {
    "code": "4",
    "status": "APPROVED",
    "scheme": "6"
  },
  "verificationCvv": {
    "code": "7",
    "status": "APPROVED",
    "scheme": "9"
  },
  "userDefined": {
    "failedPinAttempts": 3
  }
}
```







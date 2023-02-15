
# FraudRegistrationCard

| *description*: | *A JSON object that holds info about the payment registration card.*|
|----|----|
| cardholderName |    ``` string ```  <br/>  *example: John F. Doe* <br/> The cardholder name as it appears on the card.|
| cardNumber |    ``` string ```  <br/>  *example: 5424180279791732* <br/> Use this field to send clear PAN or tokens other than TransArmor Token.|
| expDate |    ``` string ```  <br/>  *example: 122028* <br/> Payment method expiration date. Format is MMYYYY.|
| cvvPresent |    ``` string ```  <br/>  *example: Y* <br/> CVV present indicator.|
| issuer |    ``` string ```  <br/>  *example: Bank of America* <br/> The company (usually a bank) that issued the card.|
| cardReissuedNumber |    ``` string ```  <br/>  *example: 2* <br/> A number that distinguishes between two plastic cards with the same card number in the event of the card being re-issued.|


**FraudRegistrationCard Example:**

```{r}

{
  "cardholderName": "John F. Doe",
  "cardNumber": "5424180279791732",
  "expDate": "122028",
  "cvvPresent": "true",
  "issuer": "Bank of America",
  "cardReissuedNumber": "2"
}
```   

  






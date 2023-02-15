
# Card

| *description*: | *Properties for the payment method.*|
|----|----|
| taToken |    ``` string ```  <br/> *example: 7591787425749818* <br/>TransArmor token value. Either the token fields or card number field must contain a value.|
| taTokenKey |  ``` string ``` <br/> *example: ab56* <br/> TransArmor token key to identify the merchant.| 
| cardholderName |    ``` string ```  <br/> *example: John F. Doe* <br/> The cardholder name as it appears on the card.
| cardNumber |  ``` string ```  <br/> *example: 5424180279791732* <br/> Use this field to send clear PAN or tokens other than TransArmor Token.|
| expDate |  ``` string ```  <br/> *example: 122028* <br/> Payment method expiration date. Format is MMYYYY.|
| cvv |  ``` string ```  <br/> *example: Y* <br/> CVV present indicator.|
| issuer |  ``` string ``` <br/> *example: Bank of America* <br/> The company (usually a bank) that issued the card.|
| cardReissuedNumber |  ``` string ``` <br/> *example: 2* <br/> A number that distinguishes between two plastic cards with the same card number in the event of the card being re-issued.|

**Card Example:**

```{r}

{
  "taToken": "7591787425749818",
  "taTokenKey": "ab56",
  "cardholderName": "John F. Doe",
  "cardNumber": "5424180279791732",
  "expDate": "122028",
  "cvv": "true",
  "issuer": "Bank of America",
  "cardReissuedNumber": "2"
}
```







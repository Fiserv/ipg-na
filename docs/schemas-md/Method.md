
# Method

| *description*: | *Info about the payment method.*|
|----|----|
| methodType* |    ``` string ```   <br/> *example: method/card* <br/> Unique ID for the payment method type. <br/> Enum:[ method/card, method/wallet ]|
| methodId |    ``` string ```  <br/> *example: 300fa792-bf5f-418e-aa74-d5b3c81298d2* <br/> The unique ID of this payment method if it was previously registered with a registration/method or if it is currently being registered. Must be unique for the entire system (not just within a specific merchant or industry). Mandatory if being used inside a registration/method.|
| methodAlias |    ``` string ```  <br/> *example: card one* <br/> The address that should be used to send billing information for this payment method.|
| card* | [Card](?path=docs/schemas-md/Card.md)|
| provider |    ``` string ```   <br/> *example: apple* <br/> The wallet provider. This field should be normalized before sending through the API.|
| userDefined |   {<br/> description: A JSON object that can carry any additional information about the customer that might be helpful for fraud detection. <br/> example:  { "phoneBrand": "samsung" }|


**Method Example:**

```{r}

{
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
}
```







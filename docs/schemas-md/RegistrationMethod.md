
# RegistrationMethod

| *description*: | *A JSON object that holds info about the payment registration method.*|
|----|----|
| methodType* |    ``` string ```  <br/>  *example: ffd031516002* <br/> Merchant reference code. Used by FirstAPI and reflected in settlement records and webhook notifications. Typically, the merchantRef field is the purchase order number or unique sequence value associated to a given transaction.|
| methodId |    ``` string ```  <br/>  *example: 300fa792-bf5f-418e-aa74-d5b3c81298d2* <br/> The unique ID of this payment method if it was previously registered with a registration/method or if it is currently being registered. Must be unique for the entire system (not just within a specific merchant or industry). Mandatory if being used inside a registration/method.|
| userDefined |   {<br/> description: A JSON object that can carry any additional information about the customer that might be helpful for fraud detection. <br/> example:  { "inauthTransId": "1234" }<br/> }|
| billingPhoneNumber |    ``` string ```  <br/>  *example: 123456789* <br/> The address that should be used to send billing information for this payment method.|
| methodAlias |    ``` string ```  <br/>  *example: card one* <br/> The address that should be used to send billing information for this payment method.|
| card* | [FraudRegistrationCard](?path=docs/schemas-md/FraudRegistrationCard.md)|
| methodAddress | [FraudAddress](?path=docs/schemas-md/FraudAddress.md)|


**RegistrationMethod Example:**

```{r}

{
  "methodType": "method/card",
  "methodId": "300fa792-bf5f-418e-aa74-d5b3c81298d2",
  "methodAlias": "card one",
  "billingPhoneNumber": "123456789",
  "userDefined": {
    "failedPinAttempts": 20
  },
  "card": {
    "cardholderName": "John F. Doe",
    "cardNumber": "5424180279791732",
    "expDate": "122028",
    "cvvPresent": "true",
    "issuer": "Bank of America",
    "cardReissuedNumber": "2"
  },
  "methodAddress": {
    "street": "125 Main Street",
    "street2": "Apartment 123",
    "stateProvince": "NY",
    "city": "New York",
    "country": "US",
    "zipPostalCode": "11375"
  }
}
``` 
  
  







# PaymentRegistration

| *description*: | *Payment Registration.*|
|----|----|
| merchantRef |    ``` string ```  <br/>  *example: ffd031516002* <br/> Merchant reference code. Used by FirstAPI and reflected in settlement records and webhook notifications. Typically, the merchantRef field is the purchase order number or unique sequence value associated to a given transaction.|
| transactionType |    ``` string ```  <br/>  *example: registration* <br/> Type of transaction merchant wants to process.|
| customer* | [Customer](?path=docs/schemas-md/Customer.md)|
| merchant* | [Merchant](?path=docs/schemas-md/Merchant.md)|
| device | [FraudRegistrationDevice](?path=docs/schemas-md/FraudRegistrationDevice.md)|
| userDefined |   {<br/> description: A JSON object that can carry any additional information about the customer that might be helpful for fraud detection. <br/> example:  { "inauthTransId": "1234" }<br/> }|
| originalTransactionType* |    ``` string ```  <br/>  *example: registration/client* <br/> Defines the type of the original transaction that is being evaluated for the Fraud Score.|
| issuerResponse | [IssuerResponse](?path=docs/schemas-md/IssuerResponse.md)|
| verificationAvs | [VerificationAvs](?path=docs/schemas-md/VerificationAvs.md)|
| verification3ds | [Verification3ds](?path=docs/schemas-md/Verification3ds.md)|
| verificationCvv | [VerificationCvv](?path=docs/schemas-md/VerificationCvv.md)|
| registrationMethod* | [RegistrationMethod](?path=docs/schemas-md/RegistrationMethod.md)|


**PaymentRegistration Example:**

```{r}

{
  "merchantRef": "ffd031516002",
  "transactionType": "registration",
  "originalTransactionType": "registration/method/card",
  "issuerResponse": {
    "code": "100",
    "status": "APPROVED",
    "scheme": "VISA"
  },
  "verificationAvs": {
    "code": "1",
    "status": "2",
    "scheme": "3"
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
  "customer": {
    "id": "125Xasdf57D",
    "startDate": "2017-01-04",
    "firstName": "John",
    "lastName": "Smith",
    "middleName": "First",
    "email": "ertpt@xyz.com",
    "sessionId": "6a2d41f5-142d-4bf1-839f-33b56dbdcf89",
    "username": "username",
    "gender": "male",
    "dateOfBirth": "2017",
    "userDefined": {
      "failedPinAttempts": "20"
    },
    "address": {
      "street": "123 Main Street",
      "street2": "Apartment 123",
      "stateProvince": "NY",
      "city": "New York",
      "country": "US",
      "phone": {
        "number": "212-515-1212"
      },
      "zipPostalCode": "11375"
    }
  },
  "merchant": {
    "merchantUniqueId": "FAPI_TEST",
    "location": {
      "locationId": "FAPI_TEST",
      "merchantAddress": {
        "street": "123 Main Street",
        "street2": "St",
        "stateProvince": "NY",
        "city": "New York",
        "country": "US",
        "zipPostalCode": "11375"
      },
      "hierarchy": "abc",
      "timeZoneOffset": "+02:00",
      "userDefined": {
        "failedPinAttempts": "20"
      }
    },
    "mcc": "7011",
    "userDefined": {
      "failedPinAttempts": "20"
    }
  },
  "device": {
    "deviceType": "device/mobile",
    "deviceId": "BDE000:008945:58AC03:F02569",
    "networks": [
      {
        "networkType": "network/wifi",
        "ip": "10.201.0.244",
        "mac": "02:00:00:00:00:00",
        "ssid": "Boston-5G-1",
        "bssid": "e8:fc:af:fb:4b:8c",
        "userDefined": {
          "battery": "5h 10m",
          "uptime": "0.95"
        }
      }
    ],
    "latitude": 90,
    "longitude": 90,
    "imei": "49-015420-323751",
    "model": "iphone",
    "manufacturer": "apple",
    "timezoneOffset": "+02:00",
    "rooted": "false",
    "malwareDetected": "false",
    "userDefined": {
      "battery": "5h 10m",
      "uptime": "0.95"
    }
  },
  "registrationMethod": {
    "methodType": "method/card",
    "methodId": "300fa792-bf5f-418e-aa74-d5b3c81298d2",
    "methodAlias": "card one",
    "card": {
      "cardholderName": "John F. Doe",
      "cardNumber": "5424180279791732",
      "expDate": "122028",
      "cvv": "true",
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
  },
  "userDefined": {
    "failedPinAttempts": "1234"
  }
}
```  
  






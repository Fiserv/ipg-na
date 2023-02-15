
# ScoreOnlyRequest

| *description*: | *Fraud detect request payload.*|
|----|----|
| merchantRef |    ``` string ```  <br/>*example: ffd031516002* <br/>Merchant reference code. Used by FirstAPI and reflected in settlement records and Webhook notifications. Typically, the merchantRef field is the purchase order number or unique sequence value associated to a given transaction.|
| transactionType* |    ``` string ```   <br/>*example: score_only* <br/>Type of transaction merchant wants to process.|
| originalTransactionType* |    ``` string ```   <br/>*example: transaction/authorization* <br/>Defines the type of the original transaction that is being evaluated for the Fraud Score. <br/> Enum:[ transaction/authorization, transaction/authorization-reversal, transaction/deposit, transaction/deposit-reversal, transaction/purchase, transaction/purchase-reversal, transaction/refund-authorization, transaction/refund-deposit, transaction/verification, transaction/balance-inquiry ]|
| originalTransactionId* |    ``` string ```   <br/> *pattern: ^(?!\s*$).+ example: fraudFAPI1231231* <br/>The unique ID of this transaction. Must be unique for the entire system (not just within a specific merchant or industry). Subsequent requests related to the same transaction must have the same transactionId (e.g. transaction/deposit or transaction/authorization-reversal). This field is used for matching transactions with settlement and chargeback information. If there is no such ID available you may wish to compose one from fields available in both systems. Consider including backend, issuer, merchant id, date and time, amount, etc. as necessary.|
| amount* |    ``` string ```   <br/>*pattern: ^(?!\s*$).+ example: 1100* <br/>The amount processed for the original transaction.|
| currencyCode* |    ``` string ```   <br/>* pattern: ([A-Z]{3})|([0-9]{3}) example: USD* <br/>The currency of the original transaction.|
| customer | [Customer](?path=docs/schemas-md/Customer.md)|  
| billingAddress | [BillingAddress](?path=docs/schemas-md/BillingAddress.md)|
| device | [Device](?path=docs/schemas-md/Device.md)|
| loyalty | [Loyalty](?path=docs/schemas-md/Loyalty.md)|
| payment* | [Payment](?path=docs/schemas-md/Payment.md)|
| merchant* | [Merchant](?path=docs/schemas-md/Merchant.md)|
| order | [FraudOrder](?path=docs/schemas-md/FraudOrder.md)|

**ScoreOnlyRequest Example:**

```{r}

{
  "merchantRef": "ffd031516002",
  "transactionType": "score_only",
  "originalTransactionType": "transaction/purchase",
  "originalTransactionId": "fraudFAPI1231231",
  "amount": "1100",
  "currencyCode": "USD",
  "customer": {
    "id": "125Xasdf57D",
    "startDate": "2017-01-04",
    "firstName": "John",
    "lastName": "Smith",
    "middleName": "First",
    "email": "accept@xyz.com",
    "sessionId": "session-1",
    "username": "username",
    "gender": "male",
    "dateOfBirth": "2017",
    "address": {
      "street": "123 Main Street",
      "street2": "Apartment 123",
      "stateProvince": "NY",
      "city": "New York",
      "country": "US",
      "phone": {
        "type": "cell",
        "number": "212-515-1212"
      },
      "zipPostalCode": "11375"
    }
  },
  "billingAddress": {
    "firstName": "John",
    "lastName": "Smith",
    "middleName": "First",
    "street": "123Mainstreet",
    "street2": "Apartment 123",
    "stateProvince": "NY",
    "city": "NewYork",
    "country": "CAN",
    "phone": {
      "type": "cell",
      "number": "212-515-1212"
    },
    "zipPostalCode": "11375"
  },
  "device": {
    "deviceType": "device/mobile",
    "deviceId": "BDE000:008945:58AC03:F02569",
    "networks": [
      {
        "networkType": "network/wifi",
        "ip": "10.201.0.244",
        "phoneNumber": "302-123-4567",
        "carrierName": "T-Mobile",
        "mobileNetworkCode": "004",
        "subscriptionIdentificationNumber": "123456789",
        "locationAreaCode": "12345",
        "cellId": "2224",
        "standard": "GSM",
        "mac": "02:00:00:00:00:00",
        "ssid": "Boston-5G-1",
        "bssid": "e8:fc:af:fb:4b:8c",
        "userDefined": {
          "battery": "5h 10m",
          "uptime": "0.95",
          "downtime": "123"
        }
      }
    ],
    "latitude": 90,
    "longitude": 90,
    "imei": "49-015420-323751",
    "model": "iphone",
    "manufacturer": "apple",
    "timezoneOffset": "+02:00",
    "rooted": false,
    "malwareDetected": false,
    "userDefined": {
      "battery": "5h 10m",
      "uptime": "0.95",
      "downtime": "123"
    }
  },
  "loyalty": {
    "id": "LY342XYS",
    "program": "GOLD",
    "balance": 200
  },
  "payment": {
    "paymentType": "payment/card",
    "method": {
      "methodType": "method/card",
      "methodId": "123",
      "methodAlias": "card_method",
      "card": {
        "taTokenKey": "ab56",
        "cardholderName": "John Smith",
        "cardNumber": "444444444444",
        "expDate": "122018",
        "cvv": "Y",
        "issuer": "Bank of America",
        "cardReissuedNumber": "3",
        "taToken": "7591787425749818"
      },
      "provider": "apple",
      "userDefined": {
        "battery": "5h 10m",
        "uptime": "0.95"
      }
    },
    "pinPresent": false,
    "entryMethod": "remote",
    "issuerResponse": {
      "code": "000",
      "status": "approved",
      "scheme": "visa"
    },
    "issuerapprovedAmount": "2468",
    "issuercardBalance": "1357",
    "verificationAvs": {
      "code": "1",
      "status": "2",
      "scheme": "3"
    },
    "verification3ds": {
      "code": "4",
      "status": "approved",
      "scheme": "6"
    },
    "verificationCvv": {
      "code": "7",
      "status": "approved",
      "scheme": "9"
    },
    "userDefined": {
      "failedPinAttempts": "20"
    }
  },
  "merchant": {
    "merchantUniqueId": "FAPI_TEST",
    "location": {
      "locationId": "FAPI_TEST",
      "merchantAddress": {
        "street": "123 Main street",
        "street2": "St",
        "stateProvince": "NY",
        "city": "New York",
        "country": "US",
        "zipPostalCode": "11375"
      },
      "timezoneOffset": "-05:00",
      "hierarchy": "abc"
    },
    "mcc": "7311"
  },
  "order": {
    "shipToAddress": {
      "phone": "123-123-1234",
      "address1": "123 Second Ave.",
      "address2": "222",
      "city": "Atlanta",
      "state": "GA",
      "zip": "30024",
      "country": "US"
    },
    "items": [
      {
        "id": "1234",
        "name": "mouse",
        "quantity": "6",
        "unit": "1",
        "unitPrice": "1299",
        "categories": [
          [
            "Books",
            "Computer",
            "Programming"
          ],
          [
            "Books",
            "Text Books",
            "Computer Science"
          ]
        ],
        "detailsUrl": "https://mystore.domain/product/978-0444751041",
        "userDefined": {
          "weight": "5021.23",
          "vat": "0.06"
        }
      }
    ],
    "detailsUrl": "https://mystore.domain/product/978-0555751041",
    "userDefined": {
      "delivery": "express",
      "carrier": "ups"
    }
  },
  "userDefined": {
    "inauthTransId": "1234"
  }
}
```







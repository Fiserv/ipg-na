
# EncryptedApplePayWalletPaymentMethod

| *description*:   | *Wallet payment method containing encrypted Apple Pay information.*|
|----|----|
| walletType |    ``` string ```  <br/>  *example: EncryptedApplePayWalletPaymentMethod|
| encryptedApplePay* | [EncryptedApplePay](?path=docs/schemas-md/EncryptedApplePay.md)|   


**EncryptedApplePayWalletPaymentMethod Example:**

```{r}

{
  "disbursementType": "DisbursementTransactionType",
  "senderInfo": {
    "name": "Franklin Sender Roosevelt",
    "streetAddress": "5565 Glenridge Connector",
    "city": "Atlanta",
    "stateCode": "GA",
    "countryCode": "US",
    "postalCode": "30342",
    "phoneNumber": "4044040740",
    "birthDate": "19560121",
    "referenceNumber": "12345678",
    "accountNumber": "135246"
  },
  "receiverInfo": {
    "name": "Abraham Receiver Lincoln",
    "streetAddress": "5565 Glenridge Connector",
    "city": "Atlanta",
    "stateCode": "GA",
    "countryCode": "US",
    "postalCode": "30342",
    "phoneNumber": "4044040740",
    "referenceNumber": "12345678",
    "accountNumber": "135246"
  }
}
``` 





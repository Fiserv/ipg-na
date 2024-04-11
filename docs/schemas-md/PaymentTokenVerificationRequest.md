
# PaymentTokenVerificationRequest

| *description*:   | *Used to request account verification using a payment token.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentTokenVerificationRequest* <br/> Object name of the account verification request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|  
| storeId |    ``` string ```  <br/> maxLength: 20  <br/> *example: 12345500000* <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| paymentToken | [UsePaymentToken](?path=docs/schemas-md/UsePaymentToken.md)|
| accountOwner | [AccountOwner](?path=docs/schemas-md/AccountOwner.md)|   

**PaymentTokenVerificationRequest Example:**

```{r}

{
    "storeId": "541634818497",
    "requestType": "PaymentTokenVerificationRequest",
    "paymentToken": {
        "value": "9988740980260042",
        "expiryDate": {
            "month": "12",
            "year": "25"
        }
    },
    "billingAddress": {
        "address1": "5565 Glenridge Conn",
        "city": "Atlanta",
        "postalCode": "30342",
        "country": "USA"
    },
    "accountOwner": {
        "firstName": "Alexander",
        "middleName": "Graham",
        "lastName": "Bell"
    }
}
```

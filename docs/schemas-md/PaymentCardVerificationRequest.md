
# PaymentCardVerificationRequest

| *description*:   | *Used to request account verification using a payment card. The expiryDate in paymentCard object is required to perform a PaymentCardVerificationRequest.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentCardVerificationRequest*  <br/> Object name of the payment schedules request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|  
| storeId |    ``` string ```  <br/>  *maxLength: 20   <br/> example: 12345500000*  <br/>  An optional outlet ID for clients that support multiple stores in the same app.|
| paymentCard | [PaymentCard](?path=docs/schemas-md/PaymentCard.md)|  
| accountOwner | [AccountOwner](?path=docs/schemas-md/AccountOwner.md)| 

**PaymentCardVerificationRequest Example:**

```{r}

{
    "requestType": "PaymentCardVerificationRequest",
    "paymentCard": {
        "cardholderName": "Pete Mitchell",
        "number": "421783XXXXXX6251",
        "expiryDate": {
            "month": "11",
            "year": "24"
        },
        "bin": "",
        "last4": "",
        "brand": "Visa",
        "securityCode": "XXX"
    },

    "accountOwner":{
        "firstName": "Pete",
        "middleName": "Maverick",
        "lastName": "Mitchell"

    },
    "billingAddress": {
        "company": "",
        "address1": "133 Oakwood Trail",
        "address2": "",
        "city": "McDonough",
        "region": "GA",
        "postalCode": "30252",
        "country": "US"
    }
}
```
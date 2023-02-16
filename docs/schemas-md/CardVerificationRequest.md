
# CardVerificationRequest

| *description*:   | *Request to verify card validity.*|
|----|----|
| paymentCard | [PaymentCard](?path=docs/schemas-md/PaymentCard.md)| 
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|
| storeId |    ``` string ```  <br/>  maxLength: 20  <br/> *example: 12345500000*. <br/>  An optional outlet ID for clients that support multiple stores in the same app.|   

**CardVerificationRequest Example:**

```{r}

{
  "paymentCard": {
    "number": "4035874000424977",
    "expiryDate": {
      "month": "12",
      "year": "25"
    },
    "securityCode": "977"
  },
  "billingAddress": {
    "address1": "5565 Glenridge Conn",
    "city": "Atlanta",
    "postalCode": "30342",
    "country": "USA"
  }
}
```

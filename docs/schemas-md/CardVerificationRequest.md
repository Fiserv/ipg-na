
# CardVerificationRequest

| *description*:   | *Request to verify card validity.*|
|----|----|
| paymentCard |  |
| billingAddress |   |
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|   

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

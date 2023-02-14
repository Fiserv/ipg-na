
# UnionPayAuthenticationUpdateRequest

| *description*:   | *Authentication update request specific to UnionPay transactions.*|
|----|----|
| storeId* |    ``` string ```  *maxLength: 20 example: 12345500000* An optional Outlet ID for clients that support multiple stores in the same developer app.|
| authenticationType* |    ``` string ```  *example: Secure3DAuthenticationUpdateRequest* Object name of the authentication update request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|
| smsVerificationCode* |    ``` string ```  *pattern: ^(?!\s*$).+ example: 111111* Customer mobile number for SMS verification.|
| securityCode* |    ``` string ```  *example: 123* Card security code if required by merchant.|


**UnionPayAuthenticationUpdateRequest Example:**

```{r}

{
  "authenticationType": "UnionPayAuthenticationUpdateRequest",
  "billingAddress": {
    "address1": "5565 Glenridge Conn",
    "city": "Atlanta",
    "postalCode": "30342",
    "country": "USA"
  },
  "securityCode": "123",
  "smsVerificationCode": "111111"
}
``` 

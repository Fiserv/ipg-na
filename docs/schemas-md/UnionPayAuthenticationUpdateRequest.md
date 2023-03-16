
# UnionPayAuthenticationUpdateRequest

| *description*:   | *Authentication update request specific to UnionPay transactions.*|
|----|----|
| storeId* |    ``` string ```  <br/>  *maxLength: 20 example: 12345500000*  <br/> An optional Outlet ID for clients that support multiple stores in the same developer app.|
| authenticationType* |    ``` string ``` <br/>   *example: Secure3DAuthenticationUpdateRequest* <br/>  Object name of the authentication update request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|
| smsVerificationCode* |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+ example: 111111* <br/>  Customer mobile number for SMS verification.|
| securityCode* |    ``` string ```  <br/>  *example: 123*  <br/> Card security code if required by merchant.|


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

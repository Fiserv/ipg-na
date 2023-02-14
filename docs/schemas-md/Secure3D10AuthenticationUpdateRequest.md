
# Secure3D10AuthenticationUpdateRequest

| *description*:   | *Authentication update request specific to 3DSecure 1.0 transactions. DEPRECATED - use Secure3DAuthenticationUpdateRequest instead*|
|----|----|
| storeId* |    ``` string ```  *maxLength: 20 example: 12345500000* An optional Outlet ID for clients that support multiple stores in the same developer app.|
| authenticationType* |    ``` string ```  *example: Secure3DAuthenticationUpdateRequest* Object name of the authentication update request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|
| payerAuthenticationResponse* |    ``` string ```  *example: eJzVWFm....9f/AhjgEcE=* A formatted message providing results of the issuer’s cardholder authentication.|
| merchantData |    ``` string ```  *example: 123* Card security code if required by merchant.|
| tokenCryptogram |  TokenCryptogramstring  *minLength: 20 maxLength: 32 example: gfgF92JHDJFjxcJHCQ23IbI12D* Network token cryptogram value.
|



**Secure3D10AuthenticationUpdateRequest Example:**

```{r}

{
  "authenticationType": "Secure3D10AuthenticationUpdateRequest",
  "billingAddress": {
    "address1": "5565 Glenridge Conn",
    "city": "Atlanta",
    "postalCode": "30342",
    "country": "USA"
  },
  "payerAuthenticationResponse": "eJzVWFm....9f/AhjgEcE=",
  "merchantData": "MD__________30002019....85bcd02599",
  "securityCode": "123"
}
``` 

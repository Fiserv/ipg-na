
# Secure3D10AuthenticationUpdateRequest

| *description*:   | *Authentication update request specific to 3DSecure 1.0 transactions.  <br/> DEPRECATED - use Secure3DAuthenticationUpdateRequest instead*|
|----|----|
| storeId* |    ``` string ```  <br/> maxLength: 20  <br/> *example: 12345500000*  <br/> An optional Outlet ID for clients that support multiple stores in the same developer app.|
| authenticationType* |    ``` string ```  <br/>  *example: Secure3DAuthenticationUpdateRequest*  <br/> Object name of the authentication update request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|
| payerAuthenticationResponse* |    ``` string ```   <br/> *example: eJzVWFm....9f/AhjgEcE=*  <br/> A formatted message providing results of the issuer’s cardholder authentication.|
| merchantData |    ``` string ```  <br/>  *example: 123*  <br/> Card security code if required by merchant.|
| tokenCryptogram |  TokenCryptogramstring  <br/> minLength: 20  <br/> maxLength: 32  <br/> *example: gfgF92JHDJFjxcJHCQ23IbI12D* <br/>  Network token cryptogram value.
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

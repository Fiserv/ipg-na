
# Secure3D21AuthenticationResult

| *description*: | *Submit the result of the authentication managed outside of the gateway for a 3-D Secure 2.x scheme. For more convenient usage without implementing 3-D Secure yourself see "authenticationRequest" section. DEPRECATED - use Secure3DAuthenticationResult instead.*| 
|----|----|
| authenticationType* |  ``` string ``` <br/> *example: Secure3DAuthenticationResult*  <br/> Specifies the version of 3DS to be used where authentication was managed outside of the gateway.|
| cavv |  ``` string ```   <br/> minLength: 20  <br/> maxLength: 32  <br/> example: AAABCZIhcQAAAABZlyFxAAAAAAA*  <br/> The Cardholder Authentication Verification Value (CAVV) is a cryptographic value derived by the issuer during payment authentication that can provide evidence of the results of payment authentication during an online purchase.|
| xid |  ``` string ```   <br/> minLength: 20  <br/> maxLength: 32  <br/> example: MfhxI43NrkuWQYLCoRWitYRDMYo*  <br/> The transaction identifier (XID) is a unique tracking number set by the merchant.|
| transactionId |  ``` string ```  <br/>  *example: f38e6948-5388-41a6-bca4-b49723c19437*  <br/> The response transaction UUID. Only applicable to MasterCard.|
| authenticationResponse |  ``` string ```   <br/> default: Y  <br/> example: A*  <br/> The result of authentication attempt returned by the 3D Secure authentication process (PaRes). <br/>  Enum:Array [6] - [ A, N, U, Y, C, R ].|
| transactionStatus |  ``` string ```   <br/> *example: A*  <br/> The transaction status as returned by the 3D Secure authentication process.  <br/> Enum:Arry [6] - [ A, N, U, Y, C, R ]|  

**Secure3D21AuthenticationResult Example:**

```{r}

{
  "requestType": "Secure3D21AuthenticationResult",
  "cavv": "AAABCZIhcQAAAABZlyFxAAAAAAA",
  "xid": "MfhxI43NrkuWQYLCoRWitYRDMYo",
  "transactionId": "f38e6948-5388-41a6-bca4-b49723c19437",
  "authenticationResponse": "Y",
  "transactionStatus": "Y"
}
```  


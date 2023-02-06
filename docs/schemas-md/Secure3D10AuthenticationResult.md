
# Secure3D10AuthenticationResult

| *description*: | *Submit the result of the authentication managed outside of the gateway for a 3-D Secure 2.x scheme. For more convenient usage without implementing 3-D Secure yourself see "authenticationRequest" section. DEPRECATED - use Secure3DAuthenticationResult instead.*|
|----|----|
| authenticationType* |  ``` string ```  *example: Secure3DAuthenticationResult.* Specifies the version of 3DS to be used where authentication was managed outside of the gateway.|
| cavv |  ``` string ```  *minLength: 20 maxLength: 32 example: AAABCZIhcQAAAABZlyFxAAAAAAA.* The Cardholder Authentication Verification Value (CAVV) is a cryptographic value derived by the issuer during payment authentication that can provide evidence of the results of payment authentication during an online purchase.|
| xid |  ``` string ```  *minLength: 20 maxLength: 32 example: MfhxI43NrkuWQYLCoRWitYRDMYo.* The transaction identifier (XID) is a unique tracking number set by the merchant.|
| transactionId |  ``` string ```  *example: f38e6948-5388-41a6-bca4-b49723c19437.* The response transaction UUID. Only applicable to MasterCard.|
| authenticationResponse |  ``` string ```  *default: Y example: A.* The result of authentication attempt returned by the 3D Secure authentication process (PaRes). Enum:Array [7] - [ A, N, U, Y, C, R ].|
| transactionStatus |  ``` string ```  *example: A.* The transaction status as returned by the 3D Secure authentication process. Enum:Arry [6] - [ A, N, U, Y, C, R ]|  

**Secure3D10AuthenticationResult Example:**

```{r}

{
  "requestType": "Secure3D10AuthenticationResult",
  "verificationResponse": "Y",
  "authenticationAttemptResult": "Y",
  "cavv": "AAABCZIhcQAAAABZlyFxAAAAAAA",
  "xid": "MfhxI43NrkuWQYLCoRWitYRDMYo"
}
```  


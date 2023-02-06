
# Secure3DAuthenticationResult

| *description*: | *Submit the result of the authentication managed outside of the gateway for a 3-D Secure 2.x scheme. For more convenient usage without implementing 3-D Secure yourself see "authenticationRequest" section.*| 
|----|----|
| authenticationType* |  ``` string ```  *example: Secure3DAuthenticationResult.* Specifies the version of 3DS to be used where authentication was managed outside of the gateway.|
| cavv |  ``` string ```  *minLength: 20 maxLength: 32 example: AAABCZIhcQAAAABZlyFxAAAAAAA.* The Cardholder Authentication Verification Value (CAVV) is a cryptographic value derived by the issuer during payment authentication that can provide evidence of the results of payment authentication during an online purchase.|
| xid |  ``` string ```  *minLength: 20 maxLength: 32 example: MfhxI43NrkuWQYLCoRWitYRDMYo.* The transaction identifier (XID) is a unique tracking number set by the merchant.|
| dsTransactionId |  ``` string ```  *example: f38e6948-5388-41a6-bca4-b49723c19437.* The response transaction UUID from the DS (directory server)|
| authenticationResponse |  ``` string ```  *default: Y example: A.* The result of authentication attempt returned by the 3D Secure authentication process (PaRes). Enum:Array [6] - [ A, N, U, Y, C, R ].|
| transactionStatus |  ``` string ```  *example: A.* The transaction status as returned by the 3D Secure authentication process. Enum:Arry [6] - [ A, N, U, Y, C, R ]|  
| messageCategory |  ``` string ```  *example: 01.* Indicates the message category of 3d secure authentication version 2.X. 01 = Payment Authentication 02 = Non-Payment Authentication 80 = Mastercard Data Only. Enum:Arry [3] - [ 01, 02, 80 ]|  

**Secure3DAuthenticationResult Example:**

```{r}

{
  "requestType": "Secure3DAuthenticationResult",
  "cavv": "AAABCZIhcQAAAABZlyFxAAAAAAA",
  "xid": "MfhxI43NrkuWQYLCoRWitYRDMYo",
  "dsTransactionId": "f38e6948-5388-41a6-bca4-b49723c19437",
  "transactionStatus": "Y",
  "messageCategory": "01"
}
```  


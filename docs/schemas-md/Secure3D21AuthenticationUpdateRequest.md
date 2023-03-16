
# Secure3D21AuthenticationUpdateRequest

| *description*: | *Authentication update request specific to 3DSecure 2.x transactions. DEPRECATED - use Secure3DAuthenticationUpdateRequest instead*| 
|----|----|
| storeId* |  ``` string ```  <br/> maxLength: 20  <br/> example: 12345500000*  <br/> An optional Outlet ID for clients that support multiple stores in the same developer app.|
| authenticationType |  ``` string ``` <br/>   *example: Secure3DAuthenticationUpdateRequest*  <br/> Object name of the authentication update request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|
| methodNotificationStatus |  ``` string ```   <br/> *example: RECEIVED*  <br/> Indicates how the merchant received the 3DS method.  <br/> Enum:[ RECEIVED, EXPECTED_BUT_NOT_RECEIVED, NOT_EXPECTED ]|
| acsResponse |  [ACSResponse](?path=docs/schemas-md/ACSResponse.md)|
| securityCode |  ``` string ```  <br/>  *example: 123* <br/>  Card security code if required by merchant.|
| tokenCryptogram |  TokenCryptogram    <br/> ``` string ```   <br/> minLength: 20  <br/> maxLength: 32 <br/>  *example: gfgF92JHDJFjxcJHCQ23IbI12D*  <br/> Network token cryptogram value.|

**Secure3D21AuthenticationUpdateRequest Example:**

```{r}

{
  "authenticationType": "Secure3D21AuthenticationUpdateRequest",
  "methodNotificationStatus": "RECEIVED"
}
```  
  


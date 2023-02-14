
# Secure3D21AuthenticationUpdateRequest

| *description*: | *Authentication update request specific to 3DSecure 2.x transactions. DEPRECATED - use Secure3DAuthenticationUpdateRequest instead*| 
|----|----|
| storeId* |  ``` string ```  *maxLength: 20 example: 12345500000* An optional Outlet ID for clients that support multiple stores in the same developer app.|
| authenticationType |  ``` string ```  *example: Secure3DAuthenticationUpdateRequest* Object name of the authentication update request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|
| methodNotificationStatus |  ``` string ```  *example: RECEIVED* Indicates how the merchant received the 3DS method. Enum:[ RECEIVED, EXPECTED_BUT_NOT_RECEIVED, NOT_EXPECTED ]|
| acsResponse |  [ACSResponse](?path=docs/schemas-md/ACSResponse.md)|
| securityCode |  ``` string ```  *example: 123* Card security code if required by merchant.|
| tokenCryptogram |  TokenCryptogram   ``` string ```  *minLength: 20 maxLength: 32 example: gfgF92JHDJFjxcJHCQ23IbI12D* Network token cryptogram value.|

**Secure3D21AuthenticationUpdateRequest Example:**

```{r}

{
  "authenticationType": "Secure3D21AuthenticationUpdateRequest",
  "methodNotificationStatus": "RECEIVED"
}
```  
  


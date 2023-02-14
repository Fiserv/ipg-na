
# AuthenticationUpdateRequest

| *description*: | *Provides shared fields for all AuthenticationUpdateRequest types. Abstract class, do not use this class directly, use one of its children.*| 
|----|----|
| storeId* |  ``` string ```  *maxLength: 20 example: 12345500000* An optional Outlet ID for clients that support multiple stores in the same developer app.|
| authenticationType |  ``` string ```  *example: Secure3DAuthenticationUpdateRequest* Object name of the authentication update request.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|

**AuthenticationUpdateRequest Example:**

```{r}

{
    "authenticationType": "Secure3DAuthenticationUpdateRequest",
    "billingAddress": OrderedMap {
        "address1": "5565 Glenridge Conn",
        "city": "Atlanta",
        "postalCode": "30342",
        "country": "USA"
    },
    "securityCode": 123,
    "merchantData": "MD123...sdfk",
    "payerAuthenticationResponse": "c7fb83b8a...73t4a827t4af8738a"
}
```  
  


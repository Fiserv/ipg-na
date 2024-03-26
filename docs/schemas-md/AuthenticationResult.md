
# AuthenticationResult

| *description*:   | *Submit the result of 3DS authentication managed outside of the gateway. <br/> An AuthenticationResult should not be submitted within the same request as an AuthenticationRequest.  <br/> Abstract class, do not use this class directly, use one of its children.*|
|----|----|
| authenticationType |     ``` string ``` <br/> *example: Secure3DAuthenticationResult*  <br/> Specifies the version of 3DS to be used where authentication was managed outside of the gateway.|

**AuthenticationRequest Example:**

```{r}

"authenticationResult": {
    "authenticationType": "Secure3D21AuthenticationResult",
    "cavv": "AAABBJkZUQAAAABXSBlRAAAAAAA=",
    "xid": "G2Q6OcsXq1k0pA0mMNHVH1P02Tw=",
    "transactionId": "f38e6948-5388-41a6-bca4-b49723c19437",
    "authenticationResponse": "Y",
    "transactionStatus": "Y"
}
```

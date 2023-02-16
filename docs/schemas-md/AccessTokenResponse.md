
# AccessTokenResponse

| *description*:   | *Access token generation response.*|
|----|----|
| tokenId |     ``` string ```  <br/> *example: gliF92ypj9cKRWUP8lpRIbI3bhNf*.  <br/> Access token for authentication.|
| status |    ``` string ```  <br/>  *example: ACTIVE*.  <br/> The token status.|
| issuedOn |    ``` string ```   <br/> *example: 1579021570941*.  <br/> Access token issued time in milliseconds.|
| expiresInSeconds |    ``` string ```   <br/> *example: 899*.  <br/> Access token expiration time.|
| publicKeyBase64 |    ``` string ```   <br/> *example: LS0tLS1CRUdJTiBQLbnFSNXRnVmc4U08LS1FTkQgUFVCTElDIEtFWS0tLS0t*.  <br/> Public key to encrypt data.|
| algorithm |    ``` string ```   <br/> *example: RSA/NONE/PKCS1PADDING*. <br/>  Encyption algorithym. One way ECDH 256 bit key.|
| clientRequestId |    ``` string ```   <br/> *example: 30dd879c-ee2f-11db-8314-0800200c9a66*. <br/>  Echoes back the value from the request header for tracking.|   

**AccessTokenResponse Example:**

```{r}

{
  "tokenId": "gliF92ypj9cKRWUP8lpRIbI3bhNf",
  "status": "ACTIVE",
  "issuedOn": "1579021570941",
  "expiresInSeconds": "899",
  "publicKeyBase64": "LS0tLS1CRUdJTiBQLbnFSNXRnVmc4U08LS1FTkQgUFVCTElDIEtFWS0tLS0t",
  "algorithm": "RSA/NONE/PKCS1PADDING",
  "clientRequestId": "30dd879c-ee2f-11db-8314-0800200c9a66"
}
```





# AccessTokenResponse

| *description*:   | *Access token generation response.*|
|----|----|
| tokenId |     ``` string ``` *example: gliF92ypj9cKRWUP8lpRIbI3bhNf*. Access token for authentication.|
| status |    ``` string ```  *example: ACTIVE*. The token status.|
| issuedOn |    ``` string ```  *example: 1579021570941*. Access token issued time in milliseconds.|
| expiresInSeconds |    ``` string ```  *example: 899*. Access token expiration time.|
| publicKeyBase64 |    ``` string ```  *example: LS0tLS1CRUdJTiBQLbnFSNXRnVmc4U08LS1FTkQgUFVCTElDIEtFWS0tLS0t*. Public key to encrypt data.|
| algorithm |    ``` string ```  *example: RSA/NONE/PKCS1PADDING*. Encyption algorithym. One way ECDH 256 bit key.|
| clientRequestId |    ``` string ```  *example: 30dd879c-ee2f-11db-8314-0800200c9a66*. Echoes back the value from the request header for tracking.|   



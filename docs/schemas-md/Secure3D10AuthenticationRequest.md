
# Secure3D10AuthenticationRequest

| *description*: | *Request authentication of the payment card using the 3DS 1.0 URL redirect scheme. DEPRECATED - use Secure3DAuthenticationRequest instead*| 
|----|----|
| authenticationType* |  ``` string ```  *example: UnionPayAuthenticationRequest.* Indicates what kind of authentication scheme the merchant wants to use on the card.|
| termURL |  ``` string ```  *maxLength: 2048 example: "https://www.mywebshop.com/process3dSecure"* The result of the authentication will be sent to this URL. If not provided, a term URL will be dynamically generated. Note this must be a valid URL (special characters should be URL-encoded).|


**Secure3D10AuthenticationRequest Example:**

```{r}

{
  "authenticationType": "Secure3D10AuthenticationRequest"
}
```  


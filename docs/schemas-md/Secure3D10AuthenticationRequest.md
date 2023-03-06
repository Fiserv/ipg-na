
# Secure3D10AuthenticationRequest

| *description*: | *Request authentication of the payment card using the 3DS 1.0 URL redirect scheme. DEPRECATED - use Secure3DAuthenticationRequest instead*| 
|----|----|
| authenticationType* |  ``` string ```  <br/>  *example: UnionPayAuthenticationRequest*  <br/> Indicates what kind of authentication scheme the merchant wants to use on the card.|
| termURL |  ``` string ```   <br/> maxLength: 2048  <br/> *example: "https://www.mywebshop.com/process3dSecure"*  <br/> The result of the authentication will be sent to this URL. If not provided, a term URL will be dynamically generated. Note this must be a valid URL (special characters should be URL-encoded).|


**Secure3D10AuthenticationRequest Example:**

```{r}

{
  "authenticationType": "Secure3D10AuthenticationRequest"
}
```  


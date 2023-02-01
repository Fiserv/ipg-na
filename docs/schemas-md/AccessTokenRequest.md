
# AccessTokenRequest

| *description*:   | *Access token generation request.*|
|----|----|
| domain |     ``` string ``` *example: somedomain.com*. Domain name.|
| token |    ``` string ```  *example: gfgF92JHDJFjxcJHCQ23IbI12D*. The token value.|
| publicKeyRequired |    ``` string ```  *example: true*. Indicates whether public key is requested or not.|  

**AccessTokenRequest Example:**

```{r}

{
  "domain": "somedomain.com",
  "token": "gfgF92JHDJFjxcJHCQ23IbI12D",
  "publicKeyRequired": false
}
```

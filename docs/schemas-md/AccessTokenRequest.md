
# AccessTokenRequest

| *description*:   | *Access token generation request.*|
|----|----|
| domain |     ``` string ``` <br/> *example: somedomain.com*.  <br/> Domain name.|
| token |    ``` string ```   <br/> *example: gfgF92JHDJFjxcJHCQ23IbI12D*.  <br/> The token value.|
| publicKeyRequired |    ``` string ```   <br/> *example: true*.  <br/> Indicates whether public key is requested or not.|  

**AccessTokenRequest Example:**

```{r}

{
  "domain": "somedomain.com",
  "token": "gfgF92JHDJFjxcJHCQ23IbI12D",
  "publicKeyRequired": false
}
```

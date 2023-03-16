
# Secure3dResponse

| *description*: | *Contains 3DSecure response code.*| 
|----|----|
| responseCode3dSecure |  ``` string ``` <br/> *example: 3*  <br/> Code received after successful payer-auth verification.|
| cardholderInfo |  ``` string ``` <br/>  maxLength: 128   <br/> *example: molestie nunc non blandit massa*  <br/>  The cardholder's information supplied by the ACS.|


**Secure3dResponse Example:**

```{r}

{
  "responseCode3dSecure": "3"
}
```  
  


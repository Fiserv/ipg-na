
# Verification3ds

| *description*: | *The result of the 3DS (3D Secure) check.*|
|----|----|
| code* |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+ <br/> *example: 4* 3DS response code.|
| status | ``` string ```   <br/>  *example: APPROVED* <br/> Interpretation of the response code.|
| scheme* | ``` string ```   <br/>  pattern: ^(?!\s*$).+ <br/> *example: amex* <br/> Identifier of the scheme.|


**Verification3ds Example:**

```{r}

{
  "code": "4",
  "status": "APPROVED",
  "scheme": "6"
}
```  






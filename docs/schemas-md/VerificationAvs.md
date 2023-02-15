
# VerificationAvs

| *description*: | *The result of the AVS (Address Verification System) check.*|
|----|----|
| code* |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+ <br/> *example: Apartment 123* First line of street address.|
| status | ``` string ```   <br/>  *example: zip match* <br/> Interpretation of the response code.|
| scheme* | ``` string ```   <br/>  pattern: ^(?!\s*$).+ <br/> *example: amex* <br/> Identifier of the scheme.|


**VerificationAvs Example:**

```{r}

{
  "code": "+Z",
  "status": "zip match",
  "scheme": "amex"
}
```  






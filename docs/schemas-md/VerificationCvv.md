
# VerificationCvv

| *description*: | *The result of the CVV (Card Verification Value, or Card Security Code) check.*|
|----|----|
| code* |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+ <br/> *example: 7* CVV response code.|
| status | ``` string ```   <br/>  *example: APPROVED* <br/> Interpretation of the response code.|
| scheme* | ``` string ```   <br/>  pattern: ^(?!\s*$).+ <br/> *example: 9* <br/> Identifier of the scheme.|


**VerificationCvv Example:**

```{r}

{
  "code": "7",
  "status": "APPROVED",
  "scheme": "9"
}
```  







# IssuerResponse

| *description*: | *The issuers response to the payment request. This field should be filled in when the message has already passed through the issuer (e.g. post-authorization).*|
|----|----|
| code* |    ``` string ```   <br/> *pattern: ^(?!\s*$).+ <br/> *example: 100* <br/> The verification response code, as sent by the verification system.|
| status |    ``` string ```  <br/> *example: approved* <br/> The interpretation of the response code. Valid values are "approved" - The verification was conducted and is approved. "declined" - The verification was conducted and is not approved. "disabled" - The verification was not conducted because it was not requested or disabled in the verification. "unknown" - The verification was attempted but it failed due to some system error (e.g. timeout). <br/> Enum:[ approved, declined, disabled, unknown ]|
| scheme* |    ``` string ```  <br/> *pattern: ^(?!\s*$).+ example: visa* <br/>  An identifier of the system/specification from which the code was received, and how the status was derived.|


**IssuerResponse Example:**

```{r}

{
  "code": "100",
  "status": "approved",
  "scheme": "VISA"
}
```







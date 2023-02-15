
# FraudRegistrationResponse

| *description*: | *FraudRegistration Response*|
|----|----|
| correlationId |    ``` string ```  <br/>  *example: 228.6277057434761* <br/> The value used to track the transaction.|
| transactionStatus |    ``` string ```  <br/>  *example: Not Processed* <br/> Status of the transaction. Valid values are 'Not Processed' and 'Scored successfully'. <br/> Enum:[ Scored Successfully, Not Processed ]|
| validationStatus |    ``` string ```  <br/>  *example: success* <br/> If status returned is "failure", input validation errors occurred. Please refer to the "Errors Section" for more info. Valid values are 'success' and 'failed'.|
| transactionType |    ``` string ```  <br/>  *example: registration* <br/> The transactionType provided in request.|
| fraudScore | [FraudScore](?path=docs/schemas-md/FraudScore.md)|
| Error | [FraudRegistrationError](?path=docs/schemas-md/FraudRegistrationError.md)|

**FraudRegistrationResponse Example:**

```{r}

{
  "correlationId": "228.6278892207286",
  "transactionStatus": "Scored Successfully",
  "validationStatus": "success",
  "transactionType": "registration",
  "fraudScore": {
    "score": "100",
    "recommendedDecision": "approve"
  }
}
```   

  






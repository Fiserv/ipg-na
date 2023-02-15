
# ScoreOnlyResponse

| *description*: | *Fraud detect response.*|
|----|----|
| correlationId |    ``` string ```  <br/>  *example: 228.9404979051319* <br/> Unique trace ID for issue triage.|
| transactionStatus | ``` string ```   <br/>  *example: Not Processed* <br/> Please refer to "Errors Section" for more info. <br/> Enum:[ Scored Successfully, Not Processed ]|
| validationStatus | ``` string ```   <br/>  *example: success* <br/> If status returned is "failure", input validation errors occurred. Please refer to the "Errors Section" for more info. Valid values are 'success' and 'failure'.|
| transactionType |    ``` string ```  <br/>  *example: transaction/authorization* <br/> The transactionType provided in request.|
| fraudScore | [fraudScore](?path=docs/schemas-md/FraudScore.md)|


**ScoreOnlyResponse Example:**

```{r}

{
  "correlationId": "228.9404979051319",
  "transactionStatus": "Not Processed",
  "validationStatus": "failure",
  "transactionType": "score_only",
  "fraudScore": {
    "score": "1000",
    "warnings": [
      "warning1",
      "warning2"
    ],
    "explanations": [
      {
        "description": "Suspicious transaction amount.",
        "type": "explanation/model"
      },
      {
        "description": "Suspicious pattern compared to number of transactions in the past 1 month for the card.",
        "type": "explanation/rule",
        "rule": "QSR_14"
      }
    ],
    "recommendedDecision": "reject"
  }
}
```  






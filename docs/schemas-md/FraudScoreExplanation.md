
# FraudScoreExplanation

| *description*: | *Explanation of the fraud score applied consisting of a description, type of the explanation, and rule (if applicable).*|
|----|----|
| description |    ``` string ```  <br/>  *example: Suspicious transaction amount.* <br/> Description of the fraud score explanation.|
| rule |    ``` string ```  <br/>  *example: QSR_14* <br/> ID of the rule being triggered.|
| type |    ``` string ```  <br/>  *example: explanation/model* <br/> Type of the explanation (model or rule).|


**FraudScoreExplanation Example:**

```{r}

{
  "description": "Suspicious pattern compared to number of transactions in the past 1 month for the card.",
  "type": "explanation/rule",
  "rule": "QSR_14"
}
```  



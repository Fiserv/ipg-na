
# FraudScore

| *description*: | *Fraud likelihood assessment consisting of a score, associated warning(s), and explanation(s) of score received.*|
|----|----|
| score |    ``` string ```  <br/>  *example: 1000* <br/> The score attributed to this request by our machine learning system, ranging from 0 (less likely to be fraud) to 1000 (more likely to be fraud).|
| warnings | [<br/> *example: List [ "warning1", "warning2" ]* <br/> A list of non-critical warnings raised while processing the request. Warnings included in this list will have integration and data-quality related messages. <br/> ```string``` <br/> example: warning1]]|
| explanations | *Explanation of the fraud score applied consisting of a description, type of the explanation, and rule (if applicable).* <br/> [[explanations](?path=docs/schemas-md/Explanations.md)]|
| recommendedDecision |    ``` string ```  <br/>  *example: accept* <br/> The action that should be taken for the request that was sent.|


**FraudScore Example:**

```{r}

{
    "score": "1000",
    "warnings": List [
        "warning1",
        "warning2"
    ],
    "explanations": List [ OrderedMap {
            "description": "Suspicious transaction amount.",
            "type": "explanation/model"
        }, OrderedMap {
            "description": "Suspicious pattern compared to number of transactions in the past 1 month for the card.",
            "type": "explanation/rule",
            "rule": "QSR_14"
        }
    ],
    "recommendedDecision": "accept"
}
```  






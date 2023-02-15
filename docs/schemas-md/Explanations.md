
# Explanations

| *description*: | *Description of the fraud score explanation.*|
|----|----|
| description |    ``` string ```  <br/>  *example:  Suspicious transaction amount.* <br/> Description of the fraud score explanation.|
| rule |    ``` string ```  <br/>  *example: QSR_14* <br/> ID of the rule being triggered.|
| type |    ``` string ```  <br/>  *example: explanation/model* <br/> Type of the explanation (model or rule).|


**Explanations Example:**

```{r}

{
    "description": "Suspicious transaction amount.",
    "type": "explanation/model"
}, OrderedMap {
    "description": "Suspicious pattern compared to number of transactions in the past 1 month for the card.",
    "type": "explanation/rule",
    "rule": "QSR_14"
}
```  







# Loyalty

| *description*: | *The loyalty program information associated with this payment.*|
|----|----|
| id |    ``` string ```   <br/> *example: AK0123456789* <br/> A unique ID associated with the loyalty program account. Must be unique within the merchants system. Depending on loyalty programs the account might also serve as a credit/bank account. If this is the case the ID must be not be the PAN.|
| program |    ``` string ```   <br/> *example: gold* <br/>A string that identifies the program in which the customer is enrolled if the merchant supports several programs or levels.|
| balance |  ``` string ```   <br/> *example: 163* <br/>The balance of the loyalty program account in a program specific currency (e.g. points).|

**Loyalty Example:**

```{r}

{
  "id": "AK0123456789",
  "program": "gold",
  "balance": 163
}
```







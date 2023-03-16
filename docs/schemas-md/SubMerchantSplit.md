
# SubMerchantSplit

| *description*:   | *Sub-merchant split object for SettlementSplit.*|
|----|----|
| merchantID* |    ``` string ```   <br/> maxLength: 15  pattern: [0-9]{1,15}  <br/> *example: 100000001*  <br/> ID of merchant for tracking.|
| amount* |    ``` number ```  <br/>  *example: 25.06*  <br/>  The amount each sub-merchant receives.|

**SubMerchantSplit Example:**

```{r}

{
  "merchantID": "100000001",
  "amount": 25.06
}
```   





 

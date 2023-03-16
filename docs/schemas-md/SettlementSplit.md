
# SettlementSplit

| *description*:   | *Sub-merchant split object for SettlementSplit.*|
|----|----|
|             | minItems: 1  maxItems: 5 example: List [  <br/> OrderedMap {  <br/> "merchantID": "100000001",  <br/> "amount": 25.06  <br/> },  <br/> OrderedMap {  <br/> "merchantID": "100000002", <br/> "amount": 15.07 <br/>  }  <br/> ]  <br/>Settle with multiple sub-merchants, sale and preAuth only.|
| merchantID* |    ``` string ```   <br/> maxLength: 15 <br/>   pattern: [0-9]{1,15}  <br/> *example: 100000001* <br/>  ID of merchant for tracking.|
| amount* |    ``` number ```  <br/>  *example: 25.06*  <br/>  The amount each sub-merchant receives.|

**SubMerchantSplit Example:**

```{r}

[
  {
    "merchantID": "100000001",
    "amount": 25.06
  },
  {
    "merchantID": "100000002",
    "amount": 15.07
  }
]
```   






 

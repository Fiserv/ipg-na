
# SettlementSplit

| *description*:   | *Sub-merchant split object for SettlementSplit.*|
|----|----|
|             | minItems: 1  maxItems: 5 example: List [ OrderedMap { "merchantID": "100000001", "amount": 25.06 }, OrderedMap { "merchantID": "100000002", "amount": 15.07 } ] Settle with multiple sub-merchants, sale and preAuth only.|
| merchantID* |    ``` string ```  *maxLength: 15  pattern: [0-9]{1,15} example: 100000001.* ID of merchant for tracking.|
| amount* |    ``` number ```  *example: 25.06*  The amount each sub-merchant receives.|

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






 

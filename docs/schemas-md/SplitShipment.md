
# SplitShipment

| *description*:   | *Split-shipment related information, in order to reuse the same authorization.*|
|----|----|
| totalCount |    ``` integer ```  *($int32)  example: 5.* Total count of the shipment, can be set at preauth or the first postauth.|
| finalShipment |    ``` integer ```  *default: false* Indicates whether the transaction is the final shipment.|

**SplitShipment Example:**

```{r}

{
  "totalCount": 1,
  "finalShipment": true
}
```   





 

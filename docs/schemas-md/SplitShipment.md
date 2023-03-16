
# SplitShipment

| *description*:   | *Split-shipment related information, in order to reuse the same authorization.*|
|----|----|
| totalCount |    ``` integer ```  <br/>  *($int32)  <br/> *example: 5*  <br/> Total count of the shipment, can be set at preauth or the first postauth.|
| finalShipment |    ``` integer ```  <br/>  <br/>  *default: false*  <br/> Indicates whether the transaction is the final shipment.|

**SplitShipment Example:**

```{r}

{
  "totalCount": 1,
  "finalShipment": true
}
```   





 

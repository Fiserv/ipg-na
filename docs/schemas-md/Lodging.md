
# Lodging

| *description*: | *Additional data specific to the lodging/hotel industry.*|
|----|----|
| arrivalDate |    ``` string ```  <br/>   *($date) <br/>  example: 2010-05-15*  <br/> Date of arrival.|
| departureDate |    ``` string ```  <br/>   *($date) <br/>  example:  2018-01-28*  <br/> Date of departure.|
| folioNumber |    ``` string ```  <br/>   *maxLength: 20  <br/> example: 12200054891* <br/>  Portfolio number.|
| extraCharges |  [ExtraCharges](?path=docs/schemas-md/ExtraCharges.md) [ example: List [ OrderedMap { "chargeItem": "MINI_BAR" }, OrderedMap { "chargeItem": "OTHER" } ] <br/> Information about charges other than base lodging.| 
| noShowIndicator |    ``` boolean ```  <br/>   *example: false*  <br/> Indicates if the transaction is associated with a delayed or no-show penalty.|

**Lodging Example:**

```{r}

{
  "arrivalDate": "2010-05-15",
  "departureDate": "2018-01-28",
  "folioNumber": "12200054891",
  "extraCharges": [
    {
      "chargeItem": "MINI_BAR"
    },
    {
      "chargeItem": "OTHER"
    }
  ],
  "noShowIndicator": false
}
```  







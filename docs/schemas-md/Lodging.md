
# Lodging

| *description*: | *Additional data specific to the lodging/hotel industry.*|
|----|----|
| arrivalDate |    ``` string ```   *($date) example: 2010-05-15* Date of arrival.|
| departureDate |    ``` string ```   *($date) example:  2018-01-28* Date of departure.|
| folioNumber |    ``` string ```   *maxLength: 20 example: 12200054891* Portfolio number.|
| extraCharges |  [ExtraCharges](?path=docs/schemas-md/ExtraCharges.md) *[ example: List [ OrderedMap { "chargeItem": "MINI_BAR" }, OrderedMap { "chargeItem": "OTHER" } ]* Information about charges other than base lodging.| 
| noShowIndicator |    ``` boolean ```   *example: false* Indicates if the transaction is associated with a delayed or no-show penalty.|

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







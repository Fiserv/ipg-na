
# Location

| *description*: | *The specific location (e.g. store or station) where the transaction takes place.*|
|----|----|
| locationId |    ``` string ```   <br/> *example: 3* <br/> The unique ID of this location.|
| merchantAddress | [FraudAddress](?path=docs/schemas-md/FraudAddress.md)|
| hierarchy |    ``` string ```  <br/> *example: FDC* <br/> Free-text field to describe a hierarchy the merchant would like to provide.|
| timezoneOffset |    ``` string ```  <br/> *example: +02:00* <br/> The timezone offset from UTC to the merchants timezone configuration, specified in the format +hh:mm.|
| userDefined |   {<br/> description: A JSON object that can carry any additional information about the customer that might be helpful for fraud detection. <br/> example:  { "phoneBrand": "samsung" }|

**Location Example:**

```{r}

{
  "locationId": "3",
  "merchantAddress": {
    "street": "5565 Glenridge Connector",
    "city": "Atlanta",
    "state": "GA",
    "zipPostalCode": "30342",
    "country": "US"
  },
  "hierarchy": "FDC",
  "timezoneOffset": "+02:00",
  "userDefined": {
    "validAddress": false
  }
}
```







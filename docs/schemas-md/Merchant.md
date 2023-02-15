
# Merchant

| *description*: | *The merchant where this transaction occurred.*|
|----|----|
| mcc |    ``` string ```  <br/> *example: 7311* <br/> The 4-digit Merchant Category Code. The merchant might be associated with multiple MCCs. In that case the MCC provided here will be the one that better describes the current transaction.|
| merchantUniqueId* |  ``` string ``` <br/> *pattern: ^(?!\s*$).+ example: 9a0f5fe8-f907-4b06-88e9-8dd5141cbf44* <br/> The unique ID of this merchant. Must be unique for the entire system (not just within a specific industry).| 
| location | [Location](?path=docs/schemas-md/Location.md)|
| userDefined |   {<br/> description: A JSON object that can carry any additional information about the customer that might be helpful for fraud detection. <br/> example:  { "highFraudVolume": true }<br/> }|

**Merchant Example:**

```{r}

{
  "mcc": "7311",
  "merchantUniqueId": "9a0f5fe8-f907-4b06-88e9-8dd5141cbf44",
  "location": {
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
  },
  "userDefined": {
    "highFraudVolume": true
  }
}
```







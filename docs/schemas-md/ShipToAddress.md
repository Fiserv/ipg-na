
# ShipToAddress

| *description*: | *The address where the items in this order should be shipped to.*|
|----|----|
| phone | [Phone](?path=docs/schemas-md/Phone.md)|
| address1 |    ``` string ```   <br/>*example: 123 Second Ave.*  <br/>First line of street address.|
| address2 |    ``` string ```   <br/>*example:  Apt #42* <br/>Second line of street address.|
| city |    ``` string ```   <br/>  *example: New York* <br/>City.|
| stateProvince |    ``` string ```   <br/> *example: NY* <br/>State or province.|
| zipPostalCode | ``` string ```  <br/> *example: 11375* <br/>Postal code.|
| country |    ``` string ```   <br/> *example: US* <br/>Country.|


**ShipToAddress Example:**

```{r}

{
  "phone": "404-404-4040",
  "address1": "5565 Glenridge Connector",
  "city": "Atlanta",
  "state": "GA",
  "zip": "30342",
  "country": "US"
}
```







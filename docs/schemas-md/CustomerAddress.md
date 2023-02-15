
# CustomerAddress

| *description*: | *Customer address fields.*|
|----|----|
| street* |    ``` string ```   <br/> pattern: ^(?!\s*$).+ <br/>*example: Apartment 123* <br/>First line of street address.|
| street2 |    ``` string ```  <br/> *example: 123 Main Street* <br/>Second line of street address.|
| stateProvince |    ``` string ```   <br/> *example: NY* <br/>State or province.|
| city |    ``` string ```   <br/>  *example: New York* <br/>City.|
| country |    ``` string ```   <br/> *example: US* <br/>Country.|
| zipPostalCode | ``` string ```  <br/> *example: 11375* <br/>Postal code.|
| phone | [Phone](?path=docs/schemas-md/Phone.md)|


**CustomerAddress Example:**

```{r}

{
  "street": "Apartment 123",
  "street2": "123 Main Street",
  "stateProvince": "NY",
  "city": "New York",
  "country": "US",
  "phone": {
    "type": "mobile",
    "number": "212-515-1212"
  },
  "zipPostalCode": "11375"
}
```








# Billing

| *description*:   | *Customer billing information.*|
|----|----|
| name |    ``` string ```    <br/> maxLength: 96  <br/> *example: John Doe*  <br/> Billing name.|
| firstName |    ``` string ```   <br/> maxLength: 48  <br/> *example: John*  <br/> Billing first name. Note - Only supported for AMEX.|
| lastName |    ``` string ```    <br/> maxLength: 48  <br/> *example: Doe* <br/>  Billing last name. Note - Only supported for AMEX.|
| customerId |    ``` string ```    <br/> maxLength: 32  <br/> *example: 1234567890*  <br/> Customer ID for billing purpose.|
| birthDate |    ``` string ```   <br/> ($date)  <br/> *example: 1980-01-31*  <br/> Customer birth date.|
| contact | [Contact](?path=docs/schemas-md/Contact.md)|
| address | [Address](?path=docs/schemas-md/Address.md)| 


**Billing Example:**

```{r}

{
  "name": "John Doe",
  "firstName": "John",
  "lastName": "Doe",
  "customerId": "1234567890",
  "address": {
    "address1": "123 Main St.",
    "city": "Sandy Springs",
    "region": "Georgia",
    "postalCode": "30303",
    "country": "USA"
  }
}
```





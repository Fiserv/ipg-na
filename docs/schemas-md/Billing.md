
# Billing

| *description*:   | *Customer billing information.*|
|----|----|
| name |    ``` string ```   *maxLength: 96 example: John Doe* Billing name.|
| firstName |    ``` string ```   *maxLength: 48 example: John* Billing first name. Note - Only supported for AMEX.|
| lastName |    ``` string ```   *maxLength: 48 example: Doe* Billing last name. Note - Only supported for AMEX.|
| customerId |    ``` string ```   *maxLength: 32 example: 1234567890* Customer ID for billing purpose.|
| birthDate |    ``` string ```   *($date) example: 1980-01-31* Customer birth date.|
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





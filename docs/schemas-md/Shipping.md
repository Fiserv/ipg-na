
# Shipping

| *description*: | *Shipping information.*|
|----|----|
| name |    ``` string ```  <br/> *example: John Doe maxLength: 96*  <br/> Name of customer for shipping.|
| contact | [Contact](?path=docs/schemas-md/Contact.md)|
| address | [Address](?path=docs/schemas-md/Address.md)|

**Shipping Example:**

```{r}

{
  "name": "John Doe",
  "contact": {
    "phone": "5555555555",
    "mobilePhone": "5555555555",
    "email": "john@test.com"
  },
  "address": {
    "address1": "123 Main St.",
    "city": "Sandy Springs",
    "region": "Georgia",
    "postalCode": "30303",
    "country": "USA"
  }
}
```





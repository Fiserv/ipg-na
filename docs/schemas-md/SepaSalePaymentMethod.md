
# SepaSalePaymentMethod

| *description*:   | *Payment method containing sepa information.*|
|----|----|
| sepa* |  [SepaSale](?path=docs/schemas-md/SepaSale.md)|


**SepaSalePaymentMethod Example:**

```{r}

{
  "sepa": {
    "iban": "DE34500100600032121604",
    "name": "John Doe",
    "email": "john.doe@test.com",
    "mandate": {
      "reference": "3RBQVEE",
      "url": "https://www.firstdata.com",
      "signatureDate": "2017-07-15",
      "type": "SINGLE"
    }
  }
}
```






# SepaSale

| *description*:   | *The payment object for SEPA Local Payment.*|
|----|----|
| iban* |    ``` string ```  *maxLength: 34 pattern: ^(?!\s*$).+ example: DE34500100600032121604* Bank account in IBAN format.|
| name* |    ``` string ```  *maxLength: 96 pattern: ^(?!\s*$).+ example: John Doe* The name of the payer.|
| email |    ``` string ```   *maxLength: 254 example: john.doe@test.com* The email address of the payer.|
| mandate |  [SepaMandate](?path=docs/schemas-md/SepaMandate.md)|      

**SepaSale Example:**

```{r}  

{{
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
```  



   



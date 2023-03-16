
# SepaSale

| *description*:   | *The payment object for SEPA Local Payment.*|
|----|----|
| iban* |    ``` string ```   <br/> maxLength: 34  <br/> pattern: ^(?!\s*$).+  <br/> *example: DE34500100600032121604* Bank account in IBAN format.|
| name* |    ``` string ```   <br/> maxLength: 96  <br/> pattern: ^(?!\s*$).+  <br/> *example: John Doe* The name of the payer.|
| email |    ``` string ```    <br/> maxLength: 254  <br/> *example: john.doe@test.com*  <br/> The email address of the payer.|
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



   



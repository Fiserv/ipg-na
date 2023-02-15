
# FraudAddress

| *description*: | *Address fields.*|
|----|----|
| street* |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+ <br/> *example: Apartment 123* First line of street address.|
| street2 | ``` string ```  <br/> *example: 123 Main Street* <br/> Second line of street address.|
| stateProvince | ``` string ```   <br/> *example: NY* <br/>  State or province.|
| city | ``` string ```  <br/> *maxLength: 96 example: Sandy Springs* City or locality.|
| country | ``` string ```  <br/> *maxLength: 32 example: USA*  <br/> ISO-3166-1 ALPHA-2, ALPHA-3, numeric or full country name. In the case of PaySecure endpoints, pass the country code in an ISO format. NOTE: Country required for following listed SEPA transactions: SEPA DD transaction done with Local Payments (aka PPRO). SEPA DD transaction done via POSEIDON and the IBAN belongs to the 'SE' country group.| 
| zipPostalCode	 | ``` string ``` <br/>  *maxLength: 24 example: 30303*  <br/> ZIP code or postal code.|


**FraudAddress Example:**

```{r}

{
  "street": "Apartment 123",
  "street2": "123 Main Street",
  "stateProvince": "NY",
  "city": "New York",
  "country": "US"
}
```  






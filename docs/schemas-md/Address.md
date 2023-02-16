
# Address

| *description*: | *Address information that is passed to the issuer (it may appear on the cardholder’s statement) or  <br/> if merchant wants to pass information that differs from the information stored on our master file.*|
|----|----|
| company |    ``` string ```  <br/> maxLength: 96  <br/> *example: Test Company*  <br/> Company name associated with the address.|
| address1 | ``` string ```  <br/>  maxLength: 96  <br/> *example: 123 Main St.*  <br/> First line of the street address.|
| address2 | ``` string ```   <br/> maxLength: 96  <br/> *example: 234 Main St.* <br/>  First line of the street address.|
| city | ``` string ```  <br/>  maxLength: 96 <br/>  *example: Sandy Springs*  <br/> City or locality.|
| region | ``` string ```  <br/>  maxLength: 96  <br/> *example: Georgia*  <br/> State or province.|
| postalCode | ``` string ```  <br/>  maxLength: 24 <br/>  *example: 30303* ZIP code or postal code.|
| country | ``` string ```  <br/>  maxLength: 32 <br/>  *example: USA*  <br/> ISO-3166-1 ALPHA-2, ALPHA-3, numeric or full country name. In the case of PaySecure endpoints, pass the country code in an ISO format. NOTE: Country required for following listed SEPA transactions: SEPA DD transaction done with Local Payments (aka PPRO). SEPA DD transaction done via POSEIDON and the IBAN belongs to the 'SE' country group.| 

**Address Example:**

```{r}

{
  "address1": "123 Main St.",
  "city": "Sandy Springs",
  "region": "Georgia",
  "postalCode": "30303",
  "country": "USA"
}
```  






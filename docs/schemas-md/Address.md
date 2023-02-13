
# Address

| *description*: | *Address information that is passed to the issuer (it may appear on the cardholder’s statement) or if merchant wants to pass information that differs from the information stored on our master file.*|
|----|----|
| company |    ``` string ```   *maxLength: 96 example: Test Company* Company name associated with the address.|
| address1 | ``` string ```  *maxLength: 96 example: 123 Main St.* First line of the street address.|
| address2 | ``` string ```  *maxLength: 96 example: 234 Main St.* First line of the street address.|
| city | ``` string ```  *maxLength: 96 example: Sandy Springs* City or locality.|
| region | ``` string ```  *maxLength: 96 example: Georgia* State or province.|
| postalCode | ``` string ```  *maxLength: 24 example: 30303* ZIP code or postal code.|
| country | ``` string ```  *maxLength: 32 example: USA* ISO-3166-1 ALPHA-2, ALPHA-3, numeric or full country name. In the case of PaySecure endpoints, pass the country code in an ISO format. NOTE: Country required for following listed SEPA transactions: SEPA DD transaction done with Local Payments (aka PPRO). SEPA DD transaction done via POSEIDON and the IBAN belongs to the 'SE' country group.| 

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






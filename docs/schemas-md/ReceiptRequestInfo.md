
# ReceiptRequestInfo

| *description*: | *Defines receipt related parameters that are necessary to generate a receipt.*|
|----|----|
| type* |    ``` string ```   *example: merchant* Defines the consumer of the receipt (e.g. cardholder, merchant). Enum:[ cardholder, merchant ]|
| locale | ``` string ```  *example: en-GB* The locale of the receipt. The format has to be a well-formed BCP 47 language tag.|
| linewidth | ``` integer ```  *default: 32 example: 48* The line width of the receipt. Default will be 32 characters.|
| city | ``` string ```  *maxLength: 96 example: Sandy Springs* City or locality.|
| region | ``` string ```  *maxLength: 96 example: Georgia* State or province.|
| postalCode | ``` string ```  *maxLength: 24 example: 30303* ZIP code or postal code.|
| country | ``` string ```  *maxLength: 32 example: USA* ISO-3166-1 ALPHA-2, ALPHA-3, numeric or full country name. In the case of PaySecure endpoints, pass the country code in an ISO format. NOTE: Country required for following listed SEPA transactions: SEPA DD transaction done with Local Payments (aka PPRO). SEPA DD transaction done via POSEIDON and the IBAN belongs to the 'SE' country group.| 

**ReceiptRequestInfo Example:**

```{r}

{
  "type": "merchant",
  "locale": "de"
}
```  








# ReceiptRequestInfo

| *description*: | *Defines receipt related parameters that are necessary to generate a receipt.*|
|----|----|
| type* |    ``` string ```  <br/> *example: merchant*  <br/> Defines the consumer of the receipt (e.g. cardholder, merchant). Enum:[ cardholder, merchant ]|
| locale | ``` string ``` <br/>   *example: en-GB* <br/>  The locale of the receipt. The format has to be a well-formed BCP 47 language tag.|
| linewidth | ``` integer ```  <br/> default: 32  <br/> *example: 48*  <br/> The line width of the receipt. Default will be 32 characters.|
| city | ``` string ```  <br/> maxLength: 96  <br/> *example: Sandy Springs*  <br/> City or locality.|
| region | ``` string ```   <br/> maxLength: 96  <br/> *example: Georgia*  <br/> State or province.|
| postalCode | ``` string ```  <br/> maxLength: 24  <br/> *example: 30303*  <br/> ZIP code or postal code.|
| country | ``` string ```  <br/> maxLength: 32  <br/> *example: USA*  <br/> ISO-3166-1 ALPHA-2, ALPHA-3, numeric or full country name. In the case of PaySecure endpoints, pass the country code in an ISO format. NOTE: Country required for following listed SEPA transactions: SEPA DD transaction done with Local Payments (aka PPRO). SEPA DD transaction done via POSEIDON and the IBAN belongs to the 'SE' country group.| 

**ReceiptRequestInfo Example:**

```{r}

{
  "type": "merchant",
  "locale": "de"
}
```  







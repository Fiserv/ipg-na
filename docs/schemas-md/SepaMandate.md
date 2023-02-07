
# SepaMandate

| *description*: | *Model for the SEPA Mandate information.*| 
|----|----|
| reference* |  ``` string ```  *maxLength: 35 pattern: [A-Za-z0-9:?/+(),. -]{1,35} example: 3RBQVEE* Existing mandate reference, managed by merchant. Must match [A-Za-z0-9:?/+(),. -]{1,35} and not start with two slashes ("//"). Also known as the mandate ID.|
| url |  ``` string ```  *maxLength: 100 pattern: ^(?!\s*$).+ example: https://www.firstdata.com* Valid URL pointing to the SEPA mandate (PDF / HTML format recommended). When your store is enabled for SEPA Direct Debit as part of the Local Payments offering, this field allows you to transmit a valid URL of SEPA Direct Debit mandate to enable the Risk and Compliance department to access the details. Please note that it is mandatory to submit a mandateReference and a mandateDate together with a mandateUrl in case you manage SEPA Direct Debit mandates on your side in the combination with the Local Payments offering.|  
| signatureDate* |  ``` string ```  *($date) example: 2017-07-15* Date of mandate signature.|
| type* |  ``` string ```  *default: SINGLE example: FINAL_COLLECTION* Sequence type of the direct debit. This defaults to 'SINGLE' if not provided. Enum:Array [ 4 ] - [ SINGLE, FIRST_COLLECTION, RECURRING_COLLECTION, FINAL_COLLECTION ]|

**SepaMandate Example:**

```{r}

{
  "reference": "3RBQVEE",
  "url": "https://www.firstdata.com",
  "signatureDate": "2017-07-15",
  "type": "SINGLE"
}
```




  






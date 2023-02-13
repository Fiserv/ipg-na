
# SubMerchantData

| *description*:   | *Once sub-merchant element is given, the transaction is considered to be a sub-merchant transaction.*|
|----|----|
| mcc* |    ``` string ```  *pattern: [0-9]{4} example: 7311* Merchant category code.|
| legalName |    ``` string ```  *maxLength: 100 example: Walmart* Inc.Store legal name.|
| email |   ``` string ```  *maxLength: 254 example: abcd.1234@fiserv.com* Sub-merchant email.|
| timezone |  ``` string ```  *maxLength: 500 example: Europe/London* Timezone.|
| address |  [Address](?path=docs/schemas-md/Address.md)|        
| document |  [Document](?path=docs/schemas-md/Document.md)|
| merchantId |   ``` string ```  * maxLength: 50  example: 987654321* Sub-merchant ID.|

**SubMerchantData Example:**

```{r}

{
  "mcc": "7311",
  "legalName": "Walmart Inc.",
  "email": "abcd.1234@fiserv.com",
  "timezone": "Europe/London",
  "address": {
    "address1": "123 Main St.",
    "city": "Sandy Springs",
    "region": "Georgia",
    "postalCode": "30303",
    "country": "USA"
  },
  "document": {
    "type": "NATIONAL_IDENTITY",
    "number": "12345666544"
  },
  "merchantId": "987654321"
}
``` 

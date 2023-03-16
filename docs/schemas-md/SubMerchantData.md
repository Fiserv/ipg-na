
# SubMerchantData

| *description*:   | *Once sub-merchant element is given, the transaction is considered to be a sub-merchant transaction.*|
|----|----|
| mcc* |    ``` string ``` <br/> *pattern: [0-9]{4}  <br/> *example: 7311*  <br/> Merchant category code.|
| legalName |    ``` string ```  <br/> maxLength: 100  <br/> *example: Walmart*  <br/> Inc.Store legal name.|
| email |   ``` string ```   <br/> maxLength: 254  <br/> example: abcd.1234@fiserv.com*  <br/> Sub-merchant email.|
| timezone |  ``` string ```   <br/> maxLength: 500  <br/> *example: Europe/London*  <br/> Timezone.|
| address |  [Address](?path=docs/schemas-md/Address.md)|        
| document |  [Document](?path=docs/schemas-md/Document.md)|
| merchantId |   ``` string ```  <br/>  maxLength: 50   <br/> *example: 987654321*  <br/> Sub-merchant ID.|

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

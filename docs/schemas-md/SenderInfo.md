
# SenderInfo

| *description*:   | *Sender information for a disbursement transaction.*|US MIDs|Non-US MIDs|
|----|----|----|----|
| name* |    ``` string ```  <br/> maxLength: 30  <br/> pattern: ^(?!\s*$).+    <br/> *example: Franklin D. Roosevelt.*  <br/> Sender name.|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|Visa: Mandatory for AFT transactions<br/>MC: Optional for funding transactions|
| streetAddress* | ``` string ```   <br/> maxLength: 50  <br/> pattern: ^(?!\s*$).+    <br/> *example: 2900 Westside Pkwy*  Sender street address.|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|Visa: Mandatory for AFT transactions<br/>MC: Optional for funding transactions|
| city* | ``` string ```   <br/> maxLength: 25  <br/> pattern: ^(?!\s*$).+    <br/> *example: Alpharetta*   <br/> Sender city.|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|Visa: Mandatory for AFT transactions<br/>MC: Optional for funding transactions|  
| stateCode* | ``` string ```  <br/> maxLength: 25  <br/> pattern: [A-Z]{2}   <br/> *example: GA*   <br/> Sender state.|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|Visa: Mandatory for AFT transactions<br/>MC: Optional for funding transactions|  
| countryCode* | ``` string ```  <br/> maxLength: 25  <br/> pattern:[A-Z]{2}    <br/> *example: USA*  <br/>  Sender country code.|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|Visa: Mandatory for AFT transactions<br/>MC: Optional for funding transactions| 
| postalCode* | ``` string ```  <br/> maxLength: 5  <br/> pattern: ^(?!\s*$).+   <br/> *example: 30004*  <br/> Sender postal code.|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|Visa: Mandatory for AFT transactions<br/>MC: Optional for funding transactions| 
| phoneNumber | ``` string ```   <br/> maxLength: 25  <br/> pattern:[0-9]{10}   <br/> example: 4044040740*  <br/> Sender phone number.|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|  
| birthDate | ``` string ```   <br/> maxLength: 25  <br/> pattern:^([0-9]{4})(1[0-2]0[1-9])(3[01]0[1-9][12][0-9])$    <br/> *example: 19560121*  <br/> Sender date of birth (YYYYMMDD).|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|  
| participationId | ``` string ```   <br/> maxLength: 30  <br/> pattern:^(?!\s*$).+    <br/> *example: 123456789123456789123456789123*|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions| 
| referenceNumber | ``` string ```   <br/> maxLength:19   <br/> pattern: ^(?!\s*$).+    <br/> *example: 123456*  Sender reference number.|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|
| accountNumber* | ``` string ```   <br/> maxLength: 19  <br/> pattern: ^(?!\s*$).+    <br/> *example: 135246*  Sender account number.|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|Visa: Mandatory for AFT transactions<br/>MC: Optional for funding transactions|
| accountType* |    ``` string ```  <br/>  *example: CARD_ACCOUNT_NO*  <br/> Enumeration values: <br/> - BANK_ACCOUNT_NO_AND_BIC <br/> - CARD_ACCOUNT_NO <br/> - IBAN <br/> - ROUTING_TRANSIT_NO_AND_BANK_ACCOUNT_NO <br/> - OTHER<br/> - EMAIL<br/> - PHONE_NUMBER<br/> - WALLET_ID<br/>- SOCIAL_NETWORK_ID|Visa: Optional for AFT transactions<br/>MC: Optional for funding transactions|Visa: Mandatory for AFT transactions<br/>MC: Optional for funding transactions|

**SenderInfo Example:**

```{r}

{
  "name": "Franklin Sender Roosevelt",
  "streetAddress": "5565 Glenridge Connector",
  "city": "Atlanta",
  "stateCode": "GA",
  "countryCode": "US",
  "postalCode": "30342",
  "phoneNumber": "4044040740",
  "birthDate": "19560121",
  "participationId": "123456789123456789123456789123",
  "referenceNumber": "12345678",
  "accountNumber": "135246",
  "accountType": "CARD_ACCOUNT_NO"
}
```




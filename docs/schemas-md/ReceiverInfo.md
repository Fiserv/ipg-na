
# ReceiverInfo

| *description*:   | *Receiver information for a funding transaction.*|US MIDs|Non-US MIDs|
|----|----|----|----|
| name* |    ``` string ```  <br/> maxLength: 70  <br/> pattern: ^(?!\s*$).+  <br/> *example: George Washington* <br/> Receiver name.|Visa: Optional for AFT transactions<br/>MC: Mandatory for funding transactions|Visa: Mandatory for AFT transactions<br/>MC: Mandatory for funding transactions|
| streetAddress | ``` string ```  <br/> maxLength: 50  <br/> pattern: ^(?!\s*$).+   <br/> *example: 2900 Westside Pkwy* <br/>   Receiver street address.|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|
| city | ``` string ```   <br/> maxLength: 25  <br/> pattern: ^(?!\s*$).+    <br/> *example: Alpharetta*  <br/>  Receiver city.|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|  
| stateCode | ``` string ```  *maxLength: 25 <br/>  pattern: [A-Z]{2}   <br/> *example: GA*  <br/>  Receiver State/Province.|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|  
| countryCode | ``` string ```  <br/>  *maxLength: 25  <br/> pattern:[A-Z]{2}    <br/> *example: USA*  <br/>  Receiver country code.|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions| 
| postalCode | ``` string ```  <br/>  *maxLength: 10  <br/> pattern: ^(?![\s-])[a-zA-Z0-9\s-]{1,9} [a-zA-Z0-9] (?![\s-])$  <br/> *example: 30342-3456*  <br/>  Receiver postal code.|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions| 
| phoneNumber | ``` string ```  <br/> *maxLength: 25  <br/> pattern:[0-9]{10}    <br/> *example: 4044040740* <br/>  Receiver phone number.|MC: Optional for funding transactions|MC: Optional for funding transactions|    
| referenceNumber | ``` string ```  <br/>  *maxLength:19   <br/> pattern: ^(?!\s*$).+    <br/> *example: 123456*  <br/>  Receiver reference number.|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|
| accountNumber | ``` string ```  <br/>  *maxLength: 19  <br/> pattern: ^(?!\s*$).+    <br/> *example: 135246*   <br/> Receiver account number.|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|
| accountType |    ``` string ```  <br/>  *example: ROUTING_TRANSIT_NO_AND_BANK_ACCOUNT_NO* <br/> This field must be available when the Receiver Account Number is present  <br/> Enumeration values: <br/> - BANK_ACCOUNT_NO_AND_BIC <br/> - CARD_ACCOUNT_NO <br/> - IBAN <br/> - ROUTING_TRANSIT_NO_AND_BANK_ACCOUNT_NO <br/> - OTHER<br/> - EMAIL<br/> - PHONE_NUMBER<br/> - WALLET_ID<br/>- SOCIAL_NETWORK_ID|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|


**ReceiverInfo Example:**

```{r}

{
  "name": "Abraham Receiver Lincoln",
  "streetAddress": "5565 Glenridge Connector",
  "city": "Atlanta",
  "stateCode": "GA",
  "countryCode": "US",
  "postalCode": "30342-3456",
  "phoneNumber": "4044040740",
  "referenceNumber": "12345678",
  "accountNumber": "135246",
  "accountType": "ROUTING_TRANSIT_NO_AND_BANK_ACCOUNT_NO"
}
```




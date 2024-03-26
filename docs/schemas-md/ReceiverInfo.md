
# ReceiverInfo

| *description*:   | *Receiver information for a funding transaction.*|
|----|----|
| name* |    ``` string ```  <br/> maxLength: 70  <br/> pattern: ^(?!\s*$).+  <br/> *example: George Washington* <br/> Receiver name.|
| streetAddress* | ``` string ```  <br/> maxLength: 50  <br/> pattern: ^(?!\s*$).+   <br/> *example: 2900 Westside Pkwy* <br/>   Sender street address.|
| city* | ``` string ```   <br/> maxLength: 25  <br/> pattern: ^(?!\s*$).+    <br/> *example: Alpharetta*  <br/>  Sender city.|  
| stateCode* | ``` string ```  *maxLength: 25 <br/>  pattern: [A-Z]{2}   <br/> *example: GA*  <br/>  Sender state.|  
| countryCode* | ``` string ```  <br/>  *maxLength: 25  <br/> pattern:[A-Z]{2}    <br/> *example: USA*  <br/>  Sender country code.| 
| postalCode* | ``` string ```  <br/>  *maxLength: 5  <br/> pattern: ^(?!\s*$).+    <br/> *example: 30004*  <br/>  Sender postal code.| 
| phoneNumber* | ``` string ```  <br/> *maxLength: 25  <br/> pattern:[0-9]{10}    <br/> *example: 4044040740* <br/>  Sender phone number.|  
| birthDate | ``` string ```   <br/> *maxLength: 25  <br/> pattern:^([0-9]{4})(1[0-2]|0[1-9])(3[01]|0[1-9]|[12][0-9])$    <br/> *example: 19560121* <br/>  Sender date of birth (YYYYMMDD).|   
| referenceNumber* | ``` string ```  <br/>  *maxLength:19   <br/> pattern: ^(?!\s*$).+    <br/> *example: 123456*  <br/>  Sender reference number.|
| accountNumber* | ``` string ```  <br/>  *maxLength: 19  <br/> pattern: ^(?!\s*$).+    <br/> *example: 135246*   <br/> Sender account number.|
| accountType |    ``` string ```  <br/>  *example: ROUTING_TRANSIT_NO_AND_BANK_ACCOUNT_NO*  <br/> Enumeration values: <br/> - BANK_ACCOUNT_NO_AND_BIC <br/> - CARD_ACCOUNT_NO <br/> - IBAN <br/> - ROUTING_TRANSIT_NO_AND_BANK_ACCOUNT_NO <br/> - OTHER<br/> - EMAIL<br/> - PHONE_NUMBER<br/> - WALLET_ID<br/>- SOCIAL_NETWORK_ID|


**ReceiverInfo Example:**

```{r}

{
  "name": "Abraham Receiver Lincoln",
  "streetAddress": "5565 Glenridge Connector",
  "city": "Atlanta",
  "stateCode": "GA",
  "countryCode": "US",
  "postalCode": "30342",
  "phoneNumber": "4044040740",
  "referenceNumber": "12345678",
  "accountNumber": "135246",
  "accountType": "ROUTING_TRANSIT_NO_AND_BANK_ACCOUNT_NO"
}
```




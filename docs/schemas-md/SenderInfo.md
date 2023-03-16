
# SenderInfo

| *description*:   | *Sender information for a disbursement transaction.*|
|----|----|
| name* |    ``` string ```  <br/> maxLength: 30  <br/> pattern: ^(?!\s*$).+    <br/> *example: Franklin D. Roosevelt.*  <br/> Sender name.|
| streetAddress* | ``` string ```   <br/> maxLength: 50  <br/> pattern: ^(?!\s*$).+    <br/> *example: 2900 Westside Pkwy*  Sender street address.|
| city* | ``` string ```   <br/> maxLength: 25  <br/> pattern: ^(?!\s*$).+    <br/> *example: Alpharetta*   <br/> Sender city.|  
| stateCode* | ``` string ```  <br/> maxLength: 25  <br/> pattern: [A-Z]{2}   <br/> *example: GA*   <br/> Sender state.|  
| countryCode* | ``` string ```  <br/> maxLength: 25  <br/> pattern:[A-Z]{2}    <br/> *example: USA*  <br/>  Sender country code.| 
| postalCode* | ``` string ```  <br/> maxLength: 5  <br/> pattern: ^(?!\s*$).+   <br/> *example: 30004*  <br/> Sender postal code.| 
| phoneNumber* | ``` string ```   <br/> maxLength: 25  <br/> pattern:[0-9]{10}   <br/> example: 4044040740*  <br/> Sender phone number.|  
| birthDate | ``` string ```   <br/> maxLength: 25  <br/> pattern:^([0-9]{4})(1[0-2]|0[1-9])(3[01]|0[1-9]|[12][0-9])$    <br/> *example: 19560121*  <br/> Sender date of birth (YYYYMMDD).|   
| referenceNumber* | ``` string ```   <br/> maxLength:19   <br/> pattern: ^(?!\s*$).+    <br/> *example: 123456*  Sender reference number.|
| accountNumber* | ``` string ```   <br/> maxLength: 19  <br/> pattern: ^(?!\s*$).+    <br/> *example: 135246*  Sender account number.|


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
  "referenceNumber": "12345678",
  "accountNumber": "135246"
}
```




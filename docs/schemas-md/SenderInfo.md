
# SenderInfo

| *description*:   | *Sender information for a disbursement transaction.*|
|----|----|
| name* |    ``` string ```  *maxLength: 30 pattern: ^(?!\s*$).+   example: Franklin D. Roosevelt.* Sender name.|
| streetAddress* | ``` string ```  *maxLength: 50 pattern: ^(?!\s*$).+   example: 2900 Westside Pkwy*  Sender street address.|
| city* | ``` string ```  *maxLength: 25 pattern: ^(?!\s*$).+   example: Alpharetta*  Sender city.|  
| stateCode* | ``` string ```  *maxLength: 25 pattern: [A-Z]{2}   example: GA*  Sender state.|  
| countryCode* | ``` string ```  *maxLength: 25 pattern:[A-Z]{2}   example: USA*  Sender country code.| 
| postalCode* | ``` string ```  *maxLength: 5 pattern: ^(?!\s*$).+   example: 30004*  Sender postal code.| 
| phoneNumber* | ``` string ```  *maxLength: 25 pattern:[0-9]{10}   example: 4044040740* Sender phone number.|  
| birthDate | ``` string ```  *maxLength: 25 pattern:^([0-9]{4})(1[0-2]|0[1-9])(3[01]|0[1-9]|[12][0-9])$   example: 19560121* Sender date of birth (YYYYMMDD).|   
| referenceNumber* | ``` string ```  *maxLength:19  pattern: ^(?!\s*$).+   example: 123456*  Sender reference number.|
| accountNumber* | ``` string ```  *maxLength: 19 pattern: ^(?!\s*$).+   example: 135246*  Sender account number.|


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




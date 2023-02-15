
# Device

| *description*: | *The device where this transaction originated.*|
|----|----|
| deviceType* |    ``` string ```   <br/> *example: device/mobile* <br/>Defines the type of this object. <br/>Enum:[ device/pos, device/mobile ]|
| deviceId* |    ``` string ```   <br/> pattern: ^(?!\s*$).+ <br/> *example: BDE000:008945:58AC03:F02569* <br/>The unique ID of the device. Must be unique for the entire system (not just within a specific merchant or industry).|
| networks |   [ <br/> example: List [ OrderedMap { "networkType": "network/wifi", "ip": "10.201.0.244", "phoneNumber": "302-123-4567", "carrierName": "T-Mobile", "mobileCountryCode": "310", "mobileNetworkCode": "004", "subscriptionIdentificationNumber": "123456789", "locationAreaCode": "12345", "cellId": "2224", "standard": "GSM", "mac": "02:00:00:00:00:00", "ssid": "Boston-5G-1", "bssid": "e8:fc:af:fb:4b:8c", "userDefined": OrderedMap { "usedData": "50MB" } } ] <br/> Information about the networks associated with the device. <br/>  [Items](?path=docs/schemas-md/Items.md) <br/>]|
| latitude |    ``` number ```   <br/> *example: 41.14961* <br/>The GPS decimal latitude, ranging from (-90.0 to 90.0) where positive numbers indicate locations North of the equator.|
| longitude |    ``` number ```  <br/> *example: -8.61099* <br/>The GPS decimal longitude, ranging from (-180.0 to 180.0) where positive numbers indicate locations East of the IERS Reference Meridian.|
| imei |    ``` string ```   <br/> *example: 49-015420-323751* <br/>The device's International Mobile Equipment Identity (IMEI) as described in IETF RFC7254.|
| model |    ``` string ```   <br/> *example: iPhone 10* <br/>The device's model name.|
| manufacturer |    ``` string ```   <br/> *example: Apple* <br/>The device's manufacturer.|
| timezoneOffset | ``` string ```  <br/> *example: +02:00* <br/>The timezone offset from UTC to the devices timezone configuration, specified in the format +hh:mm.|
| rooted | ``` boolean ```  <br/> *example: false* <br/>A flag indicating that the device has been altered to allow privileged access to users. This flag should only be set to false if a test was performed and the result was negative. Leave unset otherwise.|
| malwareDetected | ``` boolean ```  <br/> *example: false* <br/>A flag indicating that malware was detected on the mobile phone. This flag should only be set to false if a test was performed and the result was negative. Leave unset otherwise.|
| userDefined | { <br/> description: A JSON object that can carry any additional information about the device that might be helpful for fraud detection. <br/> 	}|

**Device Example:**

```{r}

{
  "deviceType": "device/mobile",
  "deviceId": "BDE000:008945:58AC03:F02569",
  "networks": {
    "networkType": "network/wifi",
    "ip": "10.201.0.244",
    "phoneNumber": "302-123-4567",
    "carrierName": "T-Mobile",
    "mobileCountryCode": "310",
    "mobileNetworkCode": "004",
    "subscriptionIdentificationNumber": "123456789",
    "locationAreaCode": "12345",
    "cellId": "2224",
    "standard": "GSM",
    "mac": "02:00:00:00:00:00",
    "ssid": "Boston-5G-1",
    "bssid": "e8:fc:af:fb:4b:8c",
    "userDefined": {
      "usedData": "50MB"
    }
  },
  "latitude": 41.14961,
  "longitude": -8.61099,
  "imei": "49-015420-323751",
  "model": "iPhone 10",
  "manufacturer": "apple",
  "timezoneOffset": "+02:00",
  "rooted": false,
  "malwareDetected": false,
  "userDefined": {
    "battery": "95%"
  }
}
```







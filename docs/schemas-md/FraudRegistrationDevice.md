
# FraudRegistrationDevice

| *description*: | *The device where this transaction originated.*|
|----|----|
| deviceType* |    ``` string ```  <br/>  *example: device/mobile* <br/> Defines the type of this object. <br/>Enum:[ device/pos, device/mobile ]|
| deviceId* |    ``` string ```  <br/>  pattern: ^(?!\s*$).+ *example: BDE000:008945:58AC03:F02569* <br/> The unique ID of the device. Must be unique for the entire system (not just within a specific merchant or industry).|
| networks | [<br/> Information about the networks associated with the device. <br/> [FraudRegistrationDeviceItems](?path=docs/schemas-md/FraudRegistrationDeviceItems.md) <br/> ]|
| latitude |    ``` string ```  *example: 41.14961* <br/> The GPS decimal latitude, ranging from (-90.0 to 90.0) where positive numbers indicate locations North of the equator.|
| longitude |    ``` number ```  *example: -8.61099* <br/> The GPS decimal longitude, ranging from (-180.0 to 180.0) where positive numbers indicate locations East of the IERS Reference Meridian.|
| imei |    ``` string ```  *example: 49-015420-323751* <br/> The device's International Mobile Equipment Identity (IMEI) as described in IETF RFC7254.|
| model |    ``` string ```  *example: iPhone 10* <br/> The device's model name.|
| manufacturer |    ``` string ```  *example: Apple* <br/> The device's manufacturer.|
| timezoneOffset |    ``` string ```  *example: +02:00* <br/> The timezone offset from UTC to the devices timezone configuration, specified in the format +hh:mm.|
| rooted |    ``` boolean ```  *example: false* <br/> A flag indicating that the device has been altered to allow privileged access to users. This flag should only be set to false if a test was performed and the result was negative. Leave unset otherwise.|
| malwareDetected |    ``` boolean ```  *example: false* <br/> A flag indicating that malware was detected on the mobile phone. This flag should only be set to false if a test was performed and the result was negative. Leave unset otherwise.|
| userDefined |   {<br/> description: A JSON object that can carry any additional information about the customer that might be helpful for fraud detection. <br/> example:  { "battery": "5h 10m"}<br/> }|


**FraudRegistrationDevice Example:**

```{r}

{
  "deviceType": "device/mobile",
  "deviceId": "BDE000:008945:58AC03:F02569",
  "networks": [
    {
      "networkType": "network/wifi",
      "ip": "10.201.0.244",
      "mac": "02:00:00:00:00:00",
      "ssid": "Boston-5G-1",
      "bssid": "e8:fc:af:fb:4b:8c",
      "userDefined": {
        "battery": "5h 10m"
      }
    }
  ],
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
  






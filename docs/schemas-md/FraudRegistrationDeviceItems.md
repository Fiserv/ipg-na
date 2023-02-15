
# FraudRegistrationDeviceItems

| *description*: | *Network information.*|
|----|----|
| networkType* |    ``` string ```  <br/>  *example: network/wifi* <br/> Defines the type of network associated with the device. <br/> Enum:[ network/mobile, network/wifi ]|
| ip |    ``` string ```  <br/> *example: 10.201.0.244* <br/> The IPv4 or IPv6 address of the device if the network assigned one.|
| mac |    ``` string ```  *example: 02:00:00:00:00:00* <br/> The MAC address of the device that is connected to the Wi-Fi network.|
| ssid |    ``` string ```  *example: Boston-5G-1* <br/> The Wi-Fi networks Service Set Identifier (SSID).|
| bssid |    ``` string ```  *example: e8:fc:af:fb:4b:8c* <br/> The Wi-Fi networks Basic Service Set Identifier (BSSID).|
| userDefined |   {<br/> description: A JSON object that can carry any additional information about the customer that might be helpful for fraud detection. <br/> example:  { "battery": "5h 10m"}|


**FraudRegistrationDeviceItems Example:**

```{r}

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
```  
  






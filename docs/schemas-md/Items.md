
# Items

| *description*: | *Network information.*|
|----|----|
| networkType |    ``` string ```  <br/> *example: network/wifi* <br/> Defines the type of network associated with the device. <br/> Enum:Array [ 2 ] - [ network/mobile, network/wifi] |
| ip |    ``` string ``` <br/> *example: 10.201.0.244* <br/> The IPv4 or IPv6 address of the device if the network assigned one.|
| phoneNumber |    ``` string ```  <br/> *example: 302-123-4567* <br/> The devices primary phone number. This value should be supplied directly without any transformation (e.g. removal of spaces, hyphens or parentheses). If this data is available in segregated fields, it should be concatenated using a blank space (" ") as a separator.|
| carrierName |    ``` string ```  <br/> *example: T-Mobile* <br/> The network carrier name.|
| mobileCountryCode |    ``` string ```  <br/> *example: 310* <br/> The Mobile Country Code (MCC) as described in the ITUs E.212 specification.|
| mobileNetworkCode |    ``` string ```  <br/> *example: 004* <br/> The Mobile Network Code (MNC) as described in the ITUs E.212 specification.|
| subscriptionIdentificationNumber |    ``` string ```  <br/> *example: 123456789* <br/> The Mobile Subscription Identification Number code (MSIN) as described in the ITUs E.212 specification.|
| locationAreaCode |    ``` string ```  <br/> *example: 12345* <br/> The Location Area Code (LAC) is a 16-bit identifier for a region that is covered by a set of network antennas.|
| cellId |    ``` string ```  <br/> *example: 2224* <br/> The Cell ID (CID) is identifier for a specific Base Transceiver Station (BTS) within a specific Location Area Code (LAC).|
| standard |    ``` string ```  <br/> *example: GSM* <br/> An identifier of the network standard used.|
| mac |    ``` string ```  <br/> *example: 02:00:00:00:00:00* <br/> The MAC address of the device that is connected to the Wi-Fi network.|
| ssid |    ``` string ```  <br/> *example: Boston-5G-1* <br/> The Wi-Fi networks Service Set Identifier (SSID).|
| bssid |    ``` string ```  <br/> *example: e8:fc:af:fb:4b:8c* <br/> The Wi-Fi networks Basic Service Set Identifier (BSSID).|
| userDefined |   {<br/> description: A JSON object that can carry any additional information about the customer that might be helpful for fraud detection. <br/> example:  { "highFraudVolume": true }<br/> }|  










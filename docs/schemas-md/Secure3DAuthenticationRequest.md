
# Secure3DAuthenticationRequest

| *description*: | *Request authentication of the payment card using the 3DS 2.x URL redirect scheme.*| 
|----|----|
| authenticationType* |  ``` string ```  *example: UnionPayAuthenticationRequest.* Indicates what kind of authentication scheme the merchant wants to use on the card.|
| termURL |  ``` string ```  *maxLength: 2048 example: "https://www.mywebshop.com/process3dSecure"* The result of the authentication will be sent to this URL. If not provided, a term URL will be dynamically generated. Note this must be a valid URL (special characters should be URL-encoded).|
| methodNotificationURL |  ``` string ```  *maxLength: 2048 example: "https://www.mywebshop.com/process3dSecureMethodNotification?transactionReferenceNumber=ffffffff-ba0b-539f-8000-016b2343ad7e"* The 3DS method iframe and transaction ID will be sent here. Note this must be a valid URL (special characters should be URL-encoded).|
| challengeIndicator |  ``` string ```  *default: 01 example: 01* Indicates whether or not a challenge should be performed. 01 = No preference (You have no preference whether a challenge should be performed. This is the default value) 02 = No challenge requested (You prefer that no challenge should be performed) 03 = Challenge requested: 3DS Requestor Preference (You prefer that a challenge should be performed) 04 = Challenge requested: Mandate (There are local or regional mandates that mean that a challenge must be performed) The following are applicable only for 3DS 2.2 protocol. 05 = No challenge requested (transactional risk analysis is already performed) 06 = No challenge requested (Data share only) 07 = No challenge requested (strong consumer authentication is already performed) 08 = No challenge requested (utilise whitelist exemption if no challenge required) 09 = Challenge requested (whitelist prompt requested if challenge required). Enum:Array [ 9 ] - [ 01, 02, 03, 04, 05, 06, 07, 08, 09 ]|
| messageCategory* |  ``` string ```  *example: 01.* Indicates the message category of 3d secure authentication version 2.X. 01 = Payment Authentication 02 = Non-Payment Authentication 80 = Mastercard Data Only. Enum:Array [ 3 ] - [ 01, 02, 80 ]|
| challengeWindowSize* |  ``` string ```  *example: 01.* Defines the size of the challenge window displayed to customers during authentication. 01 = 250 x 400 02 = 390 x 400 03 = 500 x 600 04 = 600 x 400 05 = Full screen Enum:Array [ 5 ] - [ 01, 02, 03, 04, 05 ]
| browserJavaScriptEnabled |  ``` boolean ```  *nullable: true example: true* Indicates if the browser issuing the request is capable of performing JavaScript.|
| browserJavaEnabled |  ``` boolean ```  *nullable: true example: true* Boolean that represents the ability of the cardholder browser to execute Java (required for 2.1, mandatory for 2.2 when browserjavaScriptEnabled=true)> ATTENTION - it is stronly recommended to be set (but optional at the moment for backward compatibility)|
| secure3DDeviceChannel |  ``` string ```  *nullable: true example: 02 02 = BRW 03 = 3RI Enum:Array [ 2 ] - [ 02, 03 ]* |
| secure3DThreeRIIndicator |  ``` string ```  *nullable: true example: 01  01 = Recurring transaction 02 = Instalment transaction 03 = Add card 04 = Maintain card information 05 = Account verification 06 = Split/delayed shipment 07 = Top-up 08 = Mail Order 09 = Telephone Order 10 = Whitelist status check 11 = Other payment Enum:Array [ 11 ] - [ 01, 02, 03, 04, 05, 06, 07, 08, 09, 10, 11 ]* |
| authenticationIndicator |  ``` string ```  *default: 01 example: 01*  Provides additional information to the ACS to determine the best approach for handling an authentication request. 01 = Payment transaction 02 = Recurring transaction 03 = Installment transaction 04 = Add card 05 = Maintain card 06 = Card holder verification as part of EMV token ID and Value. Enum:Array [ 6 ] - [ 01, 02, 03, 04, 05, 06 ]|
| recurringExpiry |  ``` string ```  *pattern: ^([0-9]{4})(1[0-2]|0[1-9])(3[01]|0[1-9]|[12][0-9])$  nullable: true example: 20210819* Date after which no further authorisations shall be performed.|
| recurringFrequency |  ``` integer ```  *($int32) minimum: 1 maximum: 9999 nullable: true example: 30* Indicates the minimum number of days between authorisations.|
| cardHolderBrowserParams | {[cardHolderBrowserParams](?path=docs/schemas-md/CardHolderBrowserParams.md)}|  
| skipTRA |  SkipTRA  ``` boolean ```   *default: false* skip TRA exemption for the transaction.|


**Secure3DAuthenticationRequest Example:**

```{r}

{
  "authenticationType": "Secure3DAuthenticationRequest",
  "termURL": "https://www.mywebshop.com/process3dSecure",
  "methodNotificationURL": "https://www.mywebshop.com/process3dSecureMethodNotification?transactionReferenceNumber=ffffffff-ba0b-539f-8000-016b2343ad7e",
  "challengeIndicator": "01",
  "challengeWindowSize": "01",
  "browserJavaScriptEnabled": "true",
  "browserJavaEnabled": "false",
  "secure3DDeviceChannel": "02",
  "secure3DThreeRIIndicator": "01",
  "authenticationIndicator": "01",
  "recurringExpiry": "20210804",
  "recurringFrequency": 30,
  "cardHolderBrowserParams": {
    "browserAcceptHeaders": "Accept: text/html, application/xhtml+xml, application/xml;q=0.9, image/webp, */*;q=0.8",
    "browserIP": "127.0.0.1",
    "browserLanguage": "es-419",
    "browserUserAgent": "Lynx/2.8.4rel.1 libwww-FM/2.14 SSL-MM/1.4.1 OpenSSL/0.9.6c"
  },
  "decoupledAuthenticationParams": {
    "decMaxTime": 10,
    "decReqInd": "Y"
  }
}
```  


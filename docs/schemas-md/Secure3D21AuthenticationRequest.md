
# Secure3D21AuthenticationRequest

| *description*: | *Request authentication of the payment card using the 3DS 2.x URL redirect scheme. DEPRECATED - use Secure3DAuthenticationRequest instead*| 
|----|----|
| authenticationType* |  ``` string ```  <br/>  *example: UnionPayAuthenticationRequest.*  <br/> Indicates what kind of authentication scheme the merchant wants to use on the card.|
| termURL |  ``` string ```   <br/> maxLength: 2048  <br/> *example: "https://www.mywebshop.com/process3dSecure"*  <br/> The result of the authentication will be sent to this URL. If not provided, a term URL will be dynamically generated. Note this must be a valid URL (special characters should be URL-encoded).|
| methodNotificationURL |  ``` string ```  <br/> maxLength: 2048  <br/> *example: "https://www.mywebshop.com/process3dSecureMethodNotification?transactionReferenceNumber=ffffffff-ba0b-539f-8000-016b2343ad7e"*  <br/> The 3DS method iframe and transaction ID will be sent here. Note this must be a valid URL (special characters should be URL-encoded).|
| challengeIndicator |  ``` string ```   <br/> *default: 01  <br/> example: 01*  <br/> Indicates whether or not a challenge should be performed. 01 = No preference (You have no preference whether a challenge should be performed. This is the default value) 02 = No challenge requested (You prefer that no challenge should be performed) 03 = Challenge requested: 3DS Requestor Preference (You prefer that a challenge should be performed) 04 = Challenge requested: Mandate (There are local or regional mandates that mean that a challenge must be performed) The following are applicable only for 3DS 2.2 protocol. 05 = No challenge requested (transactional risk analysis is already performed) 06 = No challenge requested (Data share only) 07 = No challenge requested (strong consumer authentication is already performed) 08 = No challenge requested (utilise whitelist exemption if no challenge required) 09 = Challenge requested (whitelist prompt requested if challenge required). Enum:Array [ 9 ] - [ 01, 02, 03, 04, 05, 06, 07, 08, 09 ]|
| authenticationResponse |  ``` string ```  <br/>  *default: Y <br/>  example: A.*  <br/> The result of authentication attempt returned by the 3D Secure authentication process (PaRes).  <br/> Enum:Array [6] - [ A, N, U, Y, C, R ].|
| challengeWindowSize |  ``` string ```   <br/> *example: 01*  <br/> Defines the size of the challenge window displayed to customers during authentication. 01 = 250 x 400 02 = 390 x 400 03 = 500 x 600 04 = 600 x 400 05 = Full screen. Enum:Array [ 5 ] - [ 01, 02, 03, 04, 05 ]|  
| browserJavaScriptEnabled |  ``` boolean ```  <br/>  *nullable: true <br/>  example: true*  <br/> Indicates if the browser issuing the request is capable of performing JavaScript.|
| browserJavaEnabled |  ``` boolean ```  *nullable: true example: true* Boolean that represents the ability of the cardholder browser to execute Java (required for 2.1, mandatory for 2.2 when browserjavaScriptEnabled=true)> ATTENTION - it is stronly recommended to be set (but optional at the moment for backward compatibility)|
| authenticationIndicator |  ``` string ```  <br/>  *default: 01  <br/> example: 01* <br/>   Provides additional information to the ACS to determine the best approach for handling an authentication request. 01 = Payment transaction 02 = Recurring transaction 03 = Installment transaction 04 = Add card 05 = Maintain card 06 = Card holder verification as part of EMV token ID and Value. Enum:Array [ 6 ] - [ 01, 02, 03, 04, 05, 06 ]|
| secure3DDeviceChannel |  ``` string ```  <br/>  *nullable: true  <br/> example: 02 02 = BRW 03 = 3RI Enum:Array [ 2 ] - [ 02, 03 ]* |
| secure3DThreeRIIndicator |  ``` string ```  <br/>  *nullable: true  <br/> example: 01  01 = Recurring transaction 02 = Instalment transaction 03 = Add card 04 = Maintain card information 05 = Account verification 06 = Split/delayed shipment 07 = Top-up 08 = Mail Order 09 = Telephone Order 10 = Whitelist status check 11 = Other payment*  <br/>  Enum:Array [ 11 ] - [ 01, 02, 03, 04, 05, 06, 07, 08, 09, 10, 11 ]* |
| recurringExpiry |  ``` string ```  <br/>  pattern: ^([0-9]{4})(1[0-2]|0[1-9])(3[01]|0[1-9]|[12][0-9])$  <br/>  nullable: true  <br/> *example: 20210819*  <br/> Date after which no further authorisations shall be performed.|
| recurringFrequency |  ``` integer ```   <br/> *($int32)  <br/> minimum: 1  <br/> maximum: 9999 <br/>  nullable: true <br/>  example: 30*  <br/> Indicates the minimum number of days between authorisations.|
| cardHolderBrowserParams | {[cardHolderBrowserParams](?path=docs/schemas-md/CardHolderBrowserParams.md)}|


**Secure3D21AuthenticationRequest Example:**

```{r}

{
  "authenticationType": "Secure3D21AuthenticationRequest",
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
  }
}
```  


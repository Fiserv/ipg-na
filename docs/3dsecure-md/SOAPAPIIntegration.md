
# 3-D Secure SOAP API Integration

## Using the Gateway API for cardholder authentication

In case you use the Gateway for 3-D Secure web based authentication, in the first step you need to submit a verification request with an *AuthenticateTransaction* parameter set to *true* and indicate which URL the result of the authentication should be sent to with using ‘TermUrl’ parameter.

If you wish to be notified about 3DS Method form display completion, you need to also submit the optional element “ThreeDSMethodNotificationURL” in your transaction request. The URL should be uniquely identifiable, so when there is a notification received on this URL, you should be able to map it with the corresponding transaction. This eliminates any dependency on the ThreeDSServerTransID, which you will receive with the 3DS Method form response. An easy way how to ensure correct transaction mapping is to is to pass a transaction reference as a query string.

For example: https://www.mywebshop.com/process3dSecureMethodNotification?transactionReferenceNumber=ffffffff-ba0b-539f-8000-016b2343ad7e

In case you would like to set the preference for the authentication flow, you can submit optional “Challenge Indicator” element with one of the values listed below. In case Challenge Indicator is not sent within your transaction request, the Gateway will populate the value “01” – No preference.

Challenge indicator available values for 3-D Secure protocol version 2.1 are:

01 = No preference (You have no preference whether a challenge should be performed. This is the default value)
02 = No challenge requested (You prefer a frictionless flow to be performed.)
03 = Challenge requested: 3-DS Requestor Preference (You prefer that a challenge should be performed)
04 = Challenge requested: Mandate (There is a regional mandates where challenge should be performed)

Challenge Indicator represents only the preference, the issuer retains the ability to make the decision on the flow type.

In case you would like to define the size of the challenge window displayed to your customers during the authentication process, you can submit optional Challenge Window Size element with one of the values listed below. 

01 = 250 x 400 
02 = 390 x 400 
03 = 500 x 600 
04 = 600 x 400 
05 = Full screen

Note: Based on the payment schemes observation it is highly recommended to use the value 05 - Full screen only for browser-based flows. Using full screen mode in app-based flows where the authentication of the cardholder happens on a smartphone or tablet might cause time-outs and trigger an error on issuer/ACS side.

In case you would like to indicate the type of authentication request, you can submit optional ThreeDSRequestorAuthenticationIndicator element in order to provide additional information to the ACS to determine the best approach for handing an authentication request:

01 = Payment transaction
04 = Add card
05 = Maintain card
06 = Card holder verification as part of EMV token ID and Value

We strongly recommend to also include billing and shipping information in your transaction request so that these details can be used in the transaction risk analysis for optimization of the EMV 3-D Secure flows.

You can also include optional CardHolderBrowserInformation element if you are able to collect such data:

```{r}

<v1:CardHolderBrowserInformation>
   <v1:BrowserAcceptHeader>Accept: text/html, application/xhtml+xml, application/xml;q=0.9, image/webp, */*;q=0.8</v1:BrowserAcceptHeader>
   <v1:BrowserIP>85.117.56.12</v1:BrowserIP>
   <v1:BrowserLanguage>es-419</v1:BrowserLanguage>
   <v1:BrowserColorDepth>32</v1:BrowserColorDepth>
   <v1:BrowserScreenHeight>1080</v1:BrowserScreenHeight>
   <v1:BrowserScreenWidth>1920</v1:BrowserScreenWidth>
   <v1:BrowserTimeZone>-300</v1:BrowserTimeZone>
   <v1:BrowserUserAgent>Lynx/2.8.4rel.1 libwww-FM/2.14 SSL-MM/1.4.1 OpenSSL/0.9.6c</v1:BrowserUserAgent>
</v1:CardHolderBrowserInformation>

```

Examples of transaction request and response can be found here: [3DS Method](?path=docs/3dsecure-md/3DSMethod.md)


## Frictionless Flow

When a transaction is considered to be a low risk transaction or an exemption is requested, a frictionless flow is applied. In such case the Gateway proceeds with the authorization without additional authentication of the cardholder.

Once the 3DS Method call has been completed, you need to notify the Gateway that the authentication process can continue by submitting the **Secure3DMethodNotificationStatus** element with the values based on corresponding conditions:

- **Secure3DMethodNotificationStatus = RECEIVED** in case you have submitted the element ThreeDSMethodNotificationURL in the initial Sale transaction request and have received the notification from ACS within 10 seconds, you will receive HTTP POST message from ACS, which will contain  a unique transaction identifier represented by threeDSServerTransID
- **Secure3DMethodNotificationStatus = EXPECTED_BUT_NOT_RECEIVED** in case you have submitted the element ThreeDSMethodNotificationURL in the initial Sale transaction request and have not received the notification from ACS within 10 seconds
- **Secure3DMethodNotificationStatus = NOT_EXPECTED** in case you have NOT submitted the element ThreeDSMethodNotificationURL in the initial Sale transaction request.

Examples of transaction request and response can be found here: [Frictionless Flow](?path=docs/3dsecure-md/3DSFrictionLessFlow.md)

## Challenge Flow

This flow is triggered, when the transaction is not considered as low risk or in case the issuer requires additional authentication of the cardholder. The whole process starts with initial Sale transaction request until the step where 3DS Method is displayed.

Once the 3DS Method call has been completed, you need to notify the Gateway that the authentication process can continue by submitting the ‘Secure3DMethodNotificationStatus’ element as explained in Frictionless Flow.

Examples of transaction request and responses can be found here: [Challenge Flow](?path=docs/3dsecure-md/ChallengeFlow.md)

In the next step you need to POST the data to the indicated URL usually implemented as auto-submit form. This needs to be implemented within your website. We recommend you to POST the challenge request element without capitals (e.g. ‘creq’) to avoid any problems in a communication with the ACS.

```{r}

<form name=frm method=POST action=https://3ds-acs.test.modirum.com/mdpayacs/creq >
  <input type=”hidden” name=”creq” value=”ewogICAiYWNzVHJhbCIgOiA...wMDAtMDAwMDAwMDA0MWE5Igp9”>
  <input type=”hidden” name=”threeDSSessionData” value=”50F2156E03083CA665BCB4..”>
</form>

```

The cardholders will be redirected to the ACS and presented with the UI to collect the authentication details - for example enter one-time-password or perform authentication using their banking app. After authentication completion the consumer is redirected back to your webpage.

After you receive the data from the ACS you need to submit them to the Gateway in ‘CRes’ element together with the reference to the original transaction: [Challenge Authentication Response](?path=docs/3dsecure-md/ChallengeAuthenticationResponse.md)

## Fallback to 3-D Secure 1.0.2 

For cases, where card issuers do not support the EMV 3DS protocol yet, the Gateway provides an option to “downgrade” to 3-D Secure 1.0.2 authentication instead. 

In the first step you submit Sale transaction request as for 3-D Secure 2.x version: [Fallback Verification](?path=docs/3dsecure-md/FallbackVerification.md)

After you have redirected the cardholder for authentication and have received the payer authentication response (PARes) from the card issuer, you submit the PARes and all mandatory elements in your next request to our API: [Fallback Authentication](?path=docs/3dsecure-md/FallbackAuthentication.md)

## API payment transactions with prior authentication through an external 3-D Secure service provider

In case you are using your own / external 3-D Secure service provider and plan to send an authorization request to the Gateway, you need to submit the values obtained during the authentication from your 3-D Secure service provider in your transaction request. 

Examples of transaction request and response can be found here: [EMV 3DS Pass-through](?path=docs/3dsecure-md/3DSPassThrough.md)

## Non-Payment Authentication (NPA)

For cases, where you would prefer to register your customers’ credit card on file without charging them in the same session, you can submit a payerAuth request to our Gateway with a value ‘02’ in “threeDSEmvCoMessageCategory” element.

As it is mandatory to use Strong Customer Authentication (SCA) for all new cards added to Card-On-File, NPA transaction request must include “ThreeDSRequestorChallengeIndicator” value ’04’ and “ThreeDSRequestorAuthenticationIndicator” value ‘04=Add card’.

The following represents an example of a ‘payerAuth’ request with basic set of elements:

```{r}

<?xml version=1.0 encoding=UTF-8?><SOAP-ENV:Envelope xmlns:SOAP-ENV=http://schemas.xmlsoap.org/soap/envelope/>
    <SOAP-ENV:Header/>
    <SOAP-ENV:Body>
        <ns4:IPGApiOrderRequest 
xmlns:ns4=http://ipg-online.com/ipgapi/schemas/ipgapi 
xmlns:ns2=http://ipg-online.com/ipgapi/schemas/v1 
xmlns:ns3=http://ipg-online.com/ipgapi/schemas/a1>
            <ns2:Transaction>
                <ns2:CreditCardTxType>
                    <ns2:StoreId>1109950006</ns2:StoreId>
                    <ns2:Type>payerAuth</ns2:Type>
                </ns2:CreditCardTxType>
                <ns2:CreditCardData>
                    <ns2:CardNumber>40169*******0014</ns2:CardNumber>
                    <ns2:ExpMonth>12</ns2:ExpMonth>
                    <ns2:ExpYear>22</ns2:ExpYear>
                    <ns2:CardCodeValue>XXX</ns2:CardCodeValue>
                </ns2:CreditCardData>
                <ns2:CreditCard3DSecure>                  
<ns2:AuthenticateTransaction>true</ns2:AuthenticateTransaction>
<ns2:ThreeDSRequestorChallengeIndicator>04</ns2:ThreeDSRequestorChallengeIndicator>              
<ns2:ThreeDSEmvCoMessageCategory>02</ns2:ThreeDSEmvCoMessageCategory>
<ns2:TermUrl>https://mywebshop.com</ns2:TermUrl>
<ns2:ThreeDSMethodNotificationURL>https://mywebshop.com/notification</ns2:ThreeDSMethodNotificationURL>
<ns2:ThreeDSRequestorChallengeWindowSize>01</ns2:ThreeDSRequestorChallengeWindowSize>
<ns2:ThreeDSRequestorAuthenticationIndicator>04</ns2:ThreeDSRequestorAuthenticationIndicator>
                </ns2:CreditCard3DSecure>                
                 <ns2:Payment>
                    <ns2:ChargeTotal>0.00</ns2:ChargeTotal>
                    <ns2:Currency>978</ns2:Currency>
                </ns2:Payment>
              </ns2:Transaction>
        </ns4:IPGApiOrderRequest>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

After this request a standard EMV 3-D Secure authentication flow as described above in Challenge Flow section follows and is completed with a final ‘payerAuth’ response:

```{r}

<SOAP-ENV:Envelope xmlns:SOAP-ENV=http://schemas.xmlsoap.org/soap/envelope/>
   <SOAP-ENV:Header/>
   <SOAP-ENV:Body>
      <ipgapi:IPGApiOrderResponse 
xmlns:a1=http://ipg-online.com/ipgapi/schemas/a1 
xmlns:ipgapi=http://ipg-online.com/ipgapi/schemas/ipgapi 
xmlns:v1=http://ipg-online.com/ipgapi/schemas/v1>
         <ipgapi:ApprovalCode>Y:ECI2/5:Authenticated</ipgapi:ApprovalCode>
         <ipgapi:Brand>VISA</ipgapi:Brand>
         <ipgapi:Country>USA</ipgapi:Country>
         <ipgapi:CommercialServiceProvider>BOSMS</ipgapi:CommercialServiceProvider>
         <ipgapi:OrderId>A-f2adf245-7a38-4729-b9e0-1fb7f1296abd</ipgapi:OrderId>
         <ipgapi:IpgTransactionId>84572410148</ipgapi:IpgTransactionId>
         <ipgapi:PaymentType>CREDITCARD</ipgapi:PaymentType>
         <ipgapi:TDate>1630925618</ipgapi:TDate>
         <ipgapi:TDateFormatted>2021.09.06 12:53:38 (CEST)</ipgapi:TDateFormatted>
         <ipgapi:TransactionResult>APPROVED</ipgapi:TransactionResult>
         <ipgapi:TransactionTime>1630925618</ipgapi:TransactionTime>
         <ipgapi:Secure3DResponse>
            <v1:ResponseCode3dSecure>1</v1:ResponseCode3dSecure>
         </ipgapi:Secure3DResponse>
      </ipgapi:IPGApiOrderResponse>
   </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

Please note, that fully authenticated NPA does not require to be authorized and cannot be used as a proof of authentication for any subsequent transactions (Recurring or MIT payments) and serves only to verify identity of your clients while adding their card on file.

 

> [Back to 3-D Secure main page](?path=docs/3dsecure-md/3DSecure.md)
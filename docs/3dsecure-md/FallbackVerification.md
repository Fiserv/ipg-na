
# EMV 3DS / Fallback to 1.0 / Verification

The following XML document represents the Sale transaction request:

```{r}

<?xml version="1.0" encoding="UTF-8"?><SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
    <SOAP-ENV:Header/>
    <SOAP-ENV:Body>
        <ns3:IPGApiOrderRequest 
xmlns:ns3="http://ipg-online.com/ipgapi/schemas/ipgapi" 
xmlns:ns2="http://ipg-online.com/ipgapi/schemas/v1" 
xmlns:ns4="http://ipg-online.com/ipgapi/schemas/a1">
            <ns2:Transaction>
                <ns2:CreditCardTxType>
                    <ns2:StoreId>120995000</ns2:StoreId>
                    <ns2:Type>sale</ns2:Type>
                </ns2:CreditCardTxType>
                <ns2:CreditCardData>
                    <ns2:CardNumber>542606XXXXXX4979</ns2:CardNumber>
                    <ns2:ExpMonth>12</ns2:ExpMonth>
                    <ns2:ExpYear>33</ns2:ExpYear>
                    <ns2:CardCodeValue>XXX</ns2:CardCodeValue>
                </ns2:CreditCardData>
                <ns2:CreditCard3DSecure>
<ns2:AuthenticateTransaction>true</ns2:AuthenticateTransaction>                         
<ns2:TermUrl>https://www.mywebshop.com/process3dSecure</ns2:TermUrl>
<ns2:ThreeDSMethodNotificationURL>https://www.mywebshop.com/process3dSecureMethodNotification</ns2:ThreeDSMethodNotificationURL>
<ns2:ThreeDSRequestorChallengeIndicator>1</ns2:ThreeDSRequestorChallengeIndicator>
                </ns2:CreditCard3DSecure>
                <ns2:Payment>
                    <ns2:ChargeTotal>13.99</ns2:ChargeTotal>
                    <ns2:Currency>978</ns2:Currency>
                </ns2:Payment>
            </ns2:Transaction>
        </ns3:IPGApiOrderRequest>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

As soon as our 3DServer identifies, that used credit card is not eligible for 2.x protocol, the Gateway automatically initiate fallback request and redirects to the dedicated DS and ACS. The Gateway then checks the card participation from the 3D Secure directory and returns the redirection URL of the card issuer’s Access Control Server (ACS).

If the card is enrolled in 3D Secure 1.0, the response usually contains the following key values:

PaReq: The Payer Authentication Request, required to initiate the authentication
ACS URL: The target of 3D Secure redirection
Term URL: The URL, that the ACS should send the outcome to in your application
*MD: Merchant Data which have to be sent to ACS URL
*Please note, that there might be cases, when MD element is not present in the response and does not have to be validated in the next step

The following represents an example of a response:

```{r}

<?xml version="1.0" encoding="UTF-8"?>
<ipgapi:IPGApiOrderResponse
xmlns:ipgapi="http://ipg-online.com/ipgapi/schemas/ipgapi" 
xmlns:a1=http://ipg-online.com/ipgapi/schemas/a1
xmlns:v1="http://ipg-online.com/ipgapi/schemas/v1">
    <ipgapi:ApprovalCode>?:waiting 3dsecure</ipgapi:ApprovalCode>
    <ipgapi:Brand>MASTERCARD</ipgapi:Brand>
    <ipgapi:Country>DEU</ipgapi:Country>
    <ipgapi:CommercialServiceProvider>RESELLER</ipgapi:CommercialServiceProvider>
    <ipgapi:OrderId>A-9278d36a-0cb1-4b6a-918b-34c723c41c6a</ipgapi:OrderId>
    <ipgapi:IpgTransactionId>84514040874</ipgapi:IpgTransactionId>
    <ipgapi:PaymentType>CREDITCARD</ipgapi:PaymentType>
    <ipgapi:TDate>1505997548</ipgapi:TDate>
    <ipgapi:TDateFormatted>2017.09.21 14:39:08 (CEST)
    </ipgapi:TDateFormatted>
    <ipgapi:TransactionTime>1505997548</ipgapi:TransactionTime>
    <ipgapi:Secure3DResponse>
        <v1:Secure3DVerificationResponse>
            <v1:VerificationRedirectResponse>
<v1:AcsURL>https://3ds-acs.test.issuer.com/mdpayacs/pareq</v1:AcsURL>              
<v1:PaReq>eJxVUslugzAQ/ZUodzA2iCWaWEqzNa...raRoFeenPMqFAFQgxk+fvahCz1</v1:PaReq>
<v1:TermUrl> https://www.mywebshop.com/process3dSecure</v1:TermUrl>
<v1:MD>MD_120020170921123……f1f3-4768-998f</v1:MD>
            </v1:VerificationRedirectResponse>
        </v1:Secure3DVerificationResponse>
    </ipgapi:Secure3DResponse>
</ipgapi:IPGApiOrderResponse>

```

> [Back to main page](?path=docs/3dsecure-md/3DSecure.md)]
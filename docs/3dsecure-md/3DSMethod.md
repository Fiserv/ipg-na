
# EMV 3DS / 3DSMethod

The following XML document represents an example of a Sale transaction request including some optional elements such ThreeDSRequestorChallengeIndicator or ThreeDSRequestorChallengeWindowSize. 

**NOTE**: *In case you submitted 'OrderId' element in your request, please make sure to include only allowed characters: A-Z, a-z, 0-9, "-" *

```{r}

<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
    xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
    <SOAP-ENV:Header/>
    <SOAP-ENV:Body>
        <ns4:IPGApiOrderRequest
            xmlns:ns4="http://ipg-online.com/ipgapi/schemas/ipgapi"
            xmlns:ns2="http://ipg-online.com/ipgapi/schemas/v1"
            xmlns:ns3="http://ipg-online.com/ipgapi/schemas/a1">
            <ns2:Transaction>
                <ns2:CreditCardTxType>
                    <ns2:StoreId>120995000</ns2:StoreId>
                    <ns2:Type>sale</ns2:Type>
                </ns2:CreditCardTxType>
                <ns2:CreditCardData>
                    <ns2:CardNumber>542606XXXXXX4979</ns2:CardNumber>
                    <ns2:ExpMonth>12</ns2:ExpMonth>
                    <ns2:ExpYear>24</ns2:ExpYear>
                    <ns2:CardCodeValue>XXX</ns2:CardCodeValue>
                </ns2:CreditCardData>
                <ns2:CreditCard3DSecure>
                    <ns2:AuthenticateTransaction>true</ns2:AuthenticateTransaction>
<ns2:TermUrl>https://www.mywebshop.com/process3dSecure/</ns2:TermUrl>
<ns2:ThreeDSMethodNotificationURL>https://www.mywebshop.com/process3dSecureMethodNotification?transactionReferenceNumber=ffff-ba0b-539f-8000-016b2343ad7e
</ns2:ThreeDSMethodNotificationURL>
<ns2:ThreeDSRequestorChallengeIndicator>01</ns2:ThreeDSRequestorChallengeIndicator>
<ns2:ThreeDSRequestorChallengeWindowSize>01</ns2:ThreeDSRequestorChallengeWindowSize>
            <ns2:CardHolderBrowserInformation>
               <ns2:BrowserAcceptHeader>Accept: text/html, application/xhtml+xml, application/xml;q=0.9, image/webp, */*;q=0.8</ns2:BrowserAcceptHeader>
               <ns2:BrowserIP>85.117.56.12</ns2:BrowserIP>
               <ns2:BrowserLanguage>es-419</ns2:BrowserLanguage>
               <ns2:BrowserColorDepth>32</ns2:BrowserColorDepth>
               <ns2:BrowserScreenHeight>1080</ns2:BrowserScreenHeight>
               <ns2:BrowserScreenWidth>1920</ns2:BrowserScreenWidth>
               <ns2:BrowserTimeZone>-300</ns2:BrowserTimeZone>
               <ns2:BrowserUserAgent>Lynx/2.8.4rel.1 libwww-FM/2.14 SSL-MM/1.4.1 OpenSSL/0.9.6c</ns2:BrowserUserAgent>
            </ns2:CardHolderBrowserInformation>
            </ns2:CreditCard3DSecure>
                <ns2:Payment>
                    <ns2:ChargeTotal>13.99</ns2:ChargeTotal>
                    <ns2:Currency>978</ns2:Currency>
                </ns2:Payment>
            </ns2:Transaction>
        </ns4:IPGApiOrderRequest>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

The response from the Gateway contains ‘3DSMethod’ element, which generates hidden iframe that helps to collect the browser data for the issuers. This information adds to the overall consumer profile and helps in identifying potentially fraudulent transactions.
You need to include the 3DSMethod in your website as hidden iframe. No user interface screen is presented to the cardholder. 

The following XML document represents an example of a response:

```{r}

<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope
    xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
    <SOAP-ENV:Header/>
    <SOAP-ENV:Body>
        <ipgapi:IPGApiOrderResponse
            xmlns:ipgapi="http://ipg-online.com/ipgapi/schemas/ipgapi"
            xmlns:a1="http://ipg-online.com/ipgapi/schemas/a1"
            xmlns:v1="http://ipg-online.com/ipgapi/schemas/v1">
            <ipgapi:ApprovalCode>?:waiting 3dsecure method</ipgapi:ApprovalCode>
            <ipgapi:Brand>MASTERCARD</ipgapi:Brand>
            <ipgapi:CommercialServiceProvider>RESELLER</ipgapi:CommercialServiceProvider>
            <ipgapi:OrderId>A-4b9804e6410b84475809e59e1b26</ipgapi:OrderId>
            <ipgapi:IpgTransactionId>8383394827</ipgapi:IpgTransactionId>
            <ipgapi:PaymentType>CREDITCARD</ipgapi:PaymentType>
            <ipgapi:TDate>1493130774</ipgapi:TDate>
            <ipgapi:TDateFormatted>2017.04.25 16:32:54(CEST)</ipgapi:TDateFormatted>
            <ipgapi:TransactionTime>1493130774</ipgapi:TransactionTime>
            <ipgapi:Secure3DResponse>
                    <v1:Secure3DMethod>
                        <v1:Secure3DMethodForm>
&lt;!DOCTYPE iframe SYSTEM "about:legacy-compat"&gt;
&lt;iframe id="tdsMmethodTgtFrame" name="tdsMmethodTgtFrame" style="width: 1px;
height: 1px; display:
none;" src="javascript:false;" xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;!--.--&gt;
&lt;/iframe&gt;&lt;form id="tdsMmethodForm" name="tdsMmethodForm"
action="https://localhost.modirum.com:8543/dstests/ACSEmu2" method="post"
target="tdsMmethodTgtFrame"
xmlns="http://www.w3.org/1999/xhtml"&gt;
&lt;input type="hidden" name="3DSMethodData"
value="eyAidGhyZWVEU1NlcnZlclRyYW5zSUQiIDogIjAwMDAwMDAwLTU2NzYtNTY2My04MDAwLTAwMDA
w&amp;#10;MDAwNDFhOSIsICJ0aHJlZURTTWV0aG9kTm90aWZpY2F0aW9uVVJMIiA6ICJodHRwczovL2xvY
2Fs&amp;#10;aG9zdC5tb2RpcnVtLmNvbTo4NTQzL21kcGF5bXBpL01lcmNoYW50U2VydmVyP21uPVkmd
HhpZD0x&amp;#10;NjgwOSZkaWdlc3Q9aSUyQnhhUEF5NWFOcVJRbllqNmozbWFDZlFJbTdFdjJYTmkwNn
h6YmZNJTJG&amp;#10;R3MlM0QiIH0"/&gt;
&lt;input type="hidden" name="threeDSMethodData"
value="eyAidGhyZWVEU1NlcnZlclRyYW5zSUQiIDogIjAwMDAwMDAwLTU2NzYtNTY2My04MDAwLTAwMDA
w&amp;#10;MDAwNDFhOSIsICJ0aHJlZURTTWV0aG9kTm90aWZpY2F0aW9uVVJMIiA6ICJodHRwczovL2xvY
2Fs&amp;#10;aG9zdC5tb2RpcnVtLmNvbTo4NTQzL21kcGF5bXBpL01lcmNoYW50U2VydmVyP21uPVkmd
HhpZD0x&amp;#10;NjgwOSZkaWdlc3Q9aSUyQnhhUEF5NWFOcVJRbllqNmozbWFDZlFJbTdFdjJYTmkwNn
h6YmZNJTJG&amp;#10;R3MlM0QiIH0"/&gt;
&lt;/form&gt;&lt;script type="text/javascript" xmlns="http://www.w3.org/1999/xhtml"&gt;
document.getElementById("tdsMmethodForm").submit();
&lt;/script&gt;
                        </v1:Secure3DMethodForm>
    <v1:ThreeDSServerTransID>3ac7caa7-aa42-2663-791b-2ac05a542c4a</v1:ThreeDSServerTransID>
                    </v1:Secure3DMethod>
            </ipgapi:Secure3DResponse>
        </ipgapi:IPGApiOrderResponse>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```


> [Back to main page](?path=docs/3dsecure-md/3DSecure.md) 


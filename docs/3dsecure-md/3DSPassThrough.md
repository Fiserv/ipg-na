
# SOAP API Authentication with external 3DS Service provider

In case you are using your own / external 3DS Service provider and plan to send authorization request to the Gateway, you need to submit the authentication values obtained from your 3DS Service provider.

The following XML document represents an example of a sale transaction submitted to our Gateway after being fully authenticated by an external service provider:

```{r}

<?xml version="1.0" encoding="UTF-8"?><ns4:IPGApiOrderRequest
xmlns:ns4="http://ipg-online.com/ipgapi/schemas/ipgapi"
xmlns:ns2="http://ipg-online.com/ipgapi/schemas/a1"
xmlns:ns3="http://ipg-online.com/ipgapi/schemas/v1">
    <ns3:Transaction>
        <ns3:CreditCardTxType>
            <ns3:Type>sale</ns3:Type>
        </ns3:CreditCardTxType>
        <ns3:CreditCardData>
            <ns3:CardNumber>403587XXXXXX4977</ns3:CardNumber>
            <ns3:ExpMonth>12</ns3:ExpMonth>
            <ns3:ExpYear>22</ns3:ExpYear>
            <ns3:CardCodeValue>XXX</ns3:CardCodeValue>
        </ns3:CreditCardData>
        <ns3:CreditCard3DSecure>
            <ns3:AuthenticationValue>AjLwsiWosla5BVgAAAA=</ns3:AuthenticationValue>
            <ns3:Secure3D2AuthenticationResponse>Y</ns3:Secure3D2AuthenticationResponse>
            <ns3:Secure3DProtocolVersion>2.1.0</ns3:Secure3DProtocolVersion>
            <ns3:DirectoryServerTransactionId>925a0317-9143-5130-8000-0000000f8742</ns3:DirectoryServerTransactionId>                 
        </ns3:CreditCard3DSecure>
        <ns3:Payment>
            <ns3:ChargeTotal>1</ns3:ChargeTotal>
            <ns3:Currency>978</ns3:Currency>
        </ns3:Payment>
        <ns3:TransactionDetails>
            <ns3:OrderId>A-123456789</ns3:OrderId>
        </ns3:TransactionDetails>
    </ns3:Transaction>
</ns4:IPGApiOrderRequest>

```

The following XML document represents an example of a response:

```{r}

<?xml version="1.0" encoding="UTF-8"?><ipgapi:IPGApiOrderResponse
xmlns:ipgapi="http://ipg-online.com/ipgapi/schemas/ipgapi"
xmlns:a1="http://ipg-online.com/ipgapi/schemas/a1"
xmlns:v1="http://ipg-online.com/ipgapi/schemas/v1">
    <ipgapi:ApprovalCode>Y:282266:8385028528:PPXM:3056131932</ipgapi:ApprovalCode>
    <ipgapi:AVSResponse>PPX</ipgapi:AVSResponse>
    <ipgapi:Brand>VISA</ipgapi:Brand>
    <ipgapi:Country>USA</ipgapi:Country>
    <ipgapi:CommercialServiceProvider>RESELLER</ipgapi:CommercialServiceProvider>
    <ipgapi:OrderId>A-123456789</ipgapi:OrderId>
    <ipgapi:IpgTransactionId>8385028528</ipgapi:IpgTransactionId>
    <ipgapi:PaymentType>CREDITCARD</ipgapi:PaymentType>
    <ipgapi:ProcessorApprovalCode>282266</ipgapi:ProcessorApprovalCode>
    <ipgapi:ProcessorReceiptNumber>1932</ipgapi:ProcessorReceiptNumber>
    <ipgapi:ProcessorCCVResponse>M</ipgapi:ProcessorCCVResponse>
    <ipgapi:ProcessorReferenceNumber>55063291</ipgapi:ProcessorReferenceNumber>
    <ipgapi:ProcessorResponseCode>00</ipgapi:ProcessorResponseCode>
    <ipgapi:ProcessorResponseMessage>Function performed error-free</ipgapi:ProcessorResponseMessage>
    <ipgapi:ProcessorTraceNumber>305613</ipgapi:ProcessorTraceNumber>
    <ipgapi:TDate>1553773696</ipgapi:TDate>
    <ipgapi:TDateFormatted>2019.03.28 12:48:16 (CET)</ipgapi:TDateFormatted>
    <ipgapi:TerminalID>54000668</ipgapi:TerminalID>
    <ipgapi:TransactionResult>APPROVED</ipgapi:TransactionResult>
    <ipgapi:TransactionTime>1553773696</ipgapi:TransactionTime>
    <ipgapi:Secure3DResponse>
        <v1:ResponseCode3dSecure>1</v1:ResponseCode3dSecure>
    </ipgapi:Secure3DResponse>
</ipgapi:IPGApiOrderResponse>

```

The following XML document represents an example of a sale transaction submitted to our Gateway after successful authentication attempt:

```{r}

<?xml version="1.0" encoding="UTF-8"?><ns4:IPGApiOrderRequest 
xmlns:ns4="http://ipg-online.com/ipgapi/schemas/ipgapi" 
xmlns:ns2="http://ipg-online.com/ipgapi/schemas/a1" 
xmlns:ns3="http://ipg-online.com/ipgapi/schemas/v1">
    <ns3:Transaction>
        <ns3:CreditCardTxType>
            <ns3:Type>sale</ns3:Type>
        </ns3:CreditCardTxType>
        <ns3:CreditCardData>
            <ns3:CardNumber>403587XXXXXX4977</ns3:CardNumber>
            <ns3:ExpMonth>12</ns3:ExpMonth>
            <ns3:ExpYear>22</ns3:ExpYear>
            <ns3:CardCodeValue>XXX</ns3:CardCodeValue>
        </ns3:CreditCardData>
        <ns3:CreditCard3DSecure>
            <ns3:AuthenticationValue>xgQO57LRAAAAAAAAAAAAAAAAAAA=</ns3:AuthenticationValue>    
            <ns3:Secure3D2AuthenticationResponse>A</ns3:Secure3D2AuthenticationResponse>
            <ns3:Secure3DProtocolVersion>2.1.0</ns3:Secure3DProtocolVersion>
            <ns3:DirectoryServerTransactionId>123456</ns3:DirectoryServerTransactionId>      
        </ns3:CreditCard3DSecure>
        <ns3:Payment>
            <ns3:ChargeTotal>1</ns3:ChargeTotal>
            <ns3:Currency>978</ns3:Currency>
        </ns3:Payment>
        <ns3:TransactionDetails>
            <ns3:OrderId>API-Test-Order12345678910</ns3:OrderId>
        </ns3:TransactionDetails>
    </ns3:Transaction>
</ns4:IPGApiOrderRequest> 

```

The following XML document represents an example of a response:

```[r}

<?xml version="1.0" encoding="UTF-8"?><ipgapi:IPGApiOrderResponse 
xmlns:ipgapi="http://ipg-online.com/ipgapi/schemas/ipgapi" 
xmlns:a1="http://ipg-online.com/ipgapi/schemas/a1" 
xmlns:v1="http://ipg-online.com/ipgapi/schemas/v1">
    <ipgapi:ApprovalCode>Y:282266:8385028528:PPXM:3056131932</ipgapi:ApprovalCode>
    <ipgapi:AVSResponse>PPX</ipgapi:AVSResponse>
    <ipgapi:Brand>VISA</ipgapi:Brand>
    <ipgapi:Country>USA</ipgapi:Country>
    <ipgapi:CommercialServiceProvider>TELECASH</ipgapi:CommercialServiceProvider>
    <ipgapi:OrderId>API-Test-Order12345678910</ipgapi:OrderId>
    <ipgapi:IpgTransactionId>8385028528</ipgapi:IpgTransactionId>
    <ipgapi:PaymentType>CREDITCARD</ipgapi:PaymentType>
    <ipgapi:ProcessorApprovalCode>282266</ipgapi:ProcessorApprovalCode>
    <ipgapi:ProcessorReceiptNumber>1932</ipgapi:ProcessorReceiptNumber>
    <ipgapi:ProcessorCCVResponse>M</ipgapi:ProcessorCCVResponse>
    <ipgapi:ProcessorReferenceNumber>55063291</ipgapi:ProcessorReferenceNumber>
    <ipgapi:ProcessorResponseCode>00</ipgapi:ProcessorResponseCode>
    <ipgapi:ProcessorResponseMessage>Function performed error-free</ipgapi:ProcessorResponseMessage>
    <ipgapi:ProcessorTraceNumber>305613</ipgapi:ProcessorTraceNumber>
    <ipgapi:TDate>1553773696</ipgapi:TDate>
    <ipgapi:TDateFormatted>2019.03.28 12:48:16 (CET)</ipgapi:TDateFormatted>
    <ipgapi:TerminalID>54000668</ipgapi:TerminalID>
    <ipgapi:TransactionResult>APPROVED</ipgapi:TransactionResult>
    <ipgapi:TransactionTime>1553773696</ipgapi:TransactionTime>
    <ipgapi:Secure3DResponse>
        <v1:ResponseCode3dSecure>4</v1:ResponseCode3dSecure>
    </ipgapi:Secure3DResponse>
</ipgapi:IPGApiOrderResponse>

```

The following ‘Secure3D2AuthenticationResponse’ element values are available:

Y = Authentication successful
U = Authentication could not be performed due to technical or other problem on DS or ACS side
A = Attempts processing performed; not authenticated, but a proof of attempted authentication is provided

Please note, that failed or rejected authentications are not to be passed to the authorization platform and will be declined by the Gateway.

|*Use Case*|*Secure 3D2 Authentication Response*|*Secure 3D2 Transaction Stauts*|*Authentication Value (CAVV/AAV)*|*IPG 3DSecure Response Code*|*Gateway Action*|
|----|----|----|----|----|----|
|Fully Authenticated Transaction <br/> (with CAVV/AAV) ECI2/ECI5|Y|Y|Value|1|The authorization message is sent to the authorization platform|
|Attempt (Successful attempt to authenticate the card holder)|A|Filed must not be submitted|Value|4|The authorization message is sent to the authorization platform|
|Unable to autheticate <br/> (The authentication is not possible on ACS or DS side)|U|Filed must not be submittedFiled must not be submitted|Filed must not be submitted|6|The authorization message is sent to the authorization platform <br/> If EC 17 Transactions are not blocked in the service configuration|

> [Back to main page](?path=docs/3dsecure-md/3DSecure.md)
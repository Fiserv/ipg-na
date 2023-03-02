
# EMV 3DS / Frictionless Flow


The following XML document represents an example of a request to be sent after 3DSMethod form display:

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
                    <ns2:StoreId>12345678</ns2:StoreId>
                    <ns2:Type>sale</ns2:Type>
                </ns2:CreditCardTxType>
                <ns2:CreditCard3DSecure>
                    <ns2:Secure3DMethodNotificationStatus>RECEIVED</ns2:Secure3DMethodNotificationStatus>
                </ns2:CreditCard3DSecure>
                <ns2:TransactionDetails>
                    <ns2:IpgTransactionId>8383394827</ns2:IpgTransactionId>
                </ns2:TransactionDetails>
            </ns2:Transaction>
        </ns4:IPGApiOrderRequest>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

The following XML document represents an example of a response you receive from the Gateway indicating, that the authorization has been successful:

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
            <ipgapi:ApprovalCode>Y:416502:0014750513:PPXM:4625106408</ipgapi:ApprovalCode>
            <ipgapi:AVSResponse>PPX</ipgapi:AVSResponse>
            <ipgapi:Brand>VISA</ipgapi:Brand>
            <ipgapi:OrderId>A-52421c39-69c4-4b2d-959d-9fdcd3a9420a</ipgapi:OrderId>
            <ipgapi:PaymentType>CREDITCARD</ipgapi:PaymentType>
            <ipgapi:ProcessorApprovalCode>416502</ipgapi:ProcessorApprovalCode>
            <ipgapi:ProcessorReceiptNumber>6408</ipgapi:ProcessorReceiptNumber>
            <ipgapi:ProcessorCCVResponse>M</ipgapi:ProcessorCCVResponse>
            <ipgapi:ProcessorTraceNumber>462510</ipgapi:ProcessorTraceNumber>
            <ipgapi:ReferencedTDate>1407373209</ipgapi:ReferencedTDate>
            <ipgapi:TDate>1407373209</ipgapi:TDate>
            <ipgapi:TDateFormatted>2014.08.07 03:00:09 (CEST)</ipgapi:TDateFormatted>
            <ipgapi:TerminalID>54000666</ipgapi:TerminalID>
            <ipgapi:Secure3DResponse>
                <v1:ResponseCode3dSecure>1</v1:ResponseCode3dSecure>
            </ipgapi:Secure3DResponse>
        </ipgapi:IPGApiOrderResponse>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

> [Back to main page](?path=docs/3dsecure-md/3DSecure.md)


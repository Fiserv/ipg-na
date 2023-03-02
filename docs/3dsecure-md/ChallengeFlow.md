
# EMV 3DS / Challenge Flow

The following XML document represents an example of a request:

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

Our Gateway verifies the response and provides the result back to you, including the challenge result data.

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
            <ipgapi:ApprovalCode>?:waiting 3dsecure</ipgapi:ApprovalCode>
            <ipgapi:Brand>MASTERCARD</ipgapi:Brand>
            <ipgapi:CommercialServiceProvider>RESELLER</ipgapi:CommercialServiceProvider>
            <ipgapi:OrderId>A-4b9804e6410b84475809e59e1b26</ipgapi:OrderId>
            <ipgapi:IpgTransactionId>8383394827</ipgapi:IpgTransactionId>
            <ipgapi:PaymentType>CREDITCARD</ipgapi:PaymentType>
            <ipgapi:TDate>1493130774</ipgapi:TDate>
            <ipgapi:TDateFormatted>2017.04.25 16:32:54(CEST)</ipgapi:TDateFormatted>
            <ipgapi:TransactionTime>1493130774</ipgapi:TransactionTime>
            <ipgapi:Secure3DResponse>
                <v1:Secure3DVerificationResponse>
                    <v1:VerificationRedirectResponse>
                        <v1:AcsURL>https://3ds-acs.issuer.com/mdpayacs/pareq</v1:AcsURL>
                        <v1:CReq>ewogICAiYWNzVHJhbCIgOiA...wMDAtMDAwMDAwMDA0MWE5Igp9</v1:CReq>
                        <v1:TermUrl>https://www.mywebshop.com/process3dSecure/</v1:TermUrl>
                        <v1:ThreeDSSessionData>50F2156E03083CA665BCB4..</v1:ThreeDSSessionData>
                    </v1:VerificationRedirectResponse>
                </v1:Secure3DVerificationResponse>
            </ipgapi:Secure3DResponse>
        </ipgapi:IPGApiOrderResponse>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

> [Back to main page](?path=docs/3dsecure-md/3DSecure.md)


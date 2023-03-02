
# EMV 3DS / Fallback to 1.0 / Authentication

The following represents an example of a request:

Please note, that in case "MD" element has not been present in the Verification response (from previous step), it will not be present in AcsResponse either.

```{r}

<?xml version="1.0" encoding="UTF-8"?>
<ipg:IPGApiOrderRequest xmlns:ipg="http://ipg-online.com/ipgapi/schemas/ipgapi">
    <v1:Transaction xmlns:v1="http://ipg-online.com/ipgapi/schemas/v1">
        <v1:CreditCardTxType>
            <v1:StoreId>120995000</v1:StoreId>
            <v1:Type>sale</v1:Type>
        </v1:CreditCardTxType>
        <v1:CreditCard3DSecure>
            <v1:Secure3DRequest>
                <v1:Secure3DAuthenticationRequest>
                   <v1:AcsResponse>
                        <v1:MD>MD_1200201709211deP2Yur……8b64-f1f3-4768-998f</v1:MD>
                        <v1:PaRes>eJzVWE.....v9/X/LjJebtlfrsCf70Y/flq/P8ARjWe/A==</v1:PaRes>
                   </v1:AcsResponse>
                </v1:Secure3DAuthenticationRequest>
            </v1:Secure3DRequest>
        </v1:CreditCard3DSecure>
        <v1:TransactionDetails>
            <v1:IpgTransactionId>84514043377</v1:IpgTransactionId>
        </v1:TransactionDetails>
    </v1:Transaction>
</ipg:IPGApiOrderRequest>

```

Our Gateway verifies the response and provides the result back to you:

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
<ipgapi:OrderId>API-Test-Order123456789</ipgapi:OrderId>
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

> [Back to main page](?path=docs/3dsecure-md/3DSecure.md)
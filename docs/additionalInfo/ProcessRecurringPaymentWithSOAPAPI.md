
# How to process Recurring Payment with SOAP API


After you have set up an agreement with your customer to initiate a recurring transaction, you have to indicate the initial payment with flagging the element "recurringType" as FIRST. 

```

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
                    <ns2:StoreId>1109950006</ns2:StoreId>
                    <ns2:Type>sale</ns2:Type>
                </ns2:CreditCardTxType>
                <ns2:CreditCardData>
                    <ns2:CardNumber>52392*****0002</ns2:CardNumber>
                    <ns2:ExpMonth>12</ns2:ExpMonth>
                    <ns2:ExpYear>22</ns2:ExpYear>
                    <ns2:CardCodeValue>XXX</ns2:CardCodeValue>
                </ns2:CreditCardData>
                <ns2:recurringType>FIRST</ns2:recurringType>
                <ns2:Payment>
                    <ns2:ChargeTotal>13.99</ns2:ChargeTotal>
                    <ns2:Currency>978</ns2:Currency>
                </ns2:Payment>
            </ns2:Transaction>
        </ns4:IPGApiOrderRequest>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

The following xml message represents an example of the response you will receive from the Gateway:

```

<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
   <SOAP-ENV:Header/>
   <SOAP-ENV:Body>
      <ipgapi:IPGApiOrderResponse xmlns:a1="http://ipg-online.com/ipgapi/schemas/a1" xmlns:ipgapi="http://ipg-online.com/ipgapi/schemas/ipgapi" xmlns:v1="http://ipg-online.com/ipgapi/schemas/v1">
         <ipgapi:ApprovalCode>Y:403939:4566959508:YYYM:441809</ipgapi:ApprovalCode>
         <ipgapi:AVSResponse>YYY</ipgapi:AVSResponse>
         <ipgapi:Brand>MASTERCARD</ipgapi:Brand>
         <ipgapi:CommercialServiceProvider>BOSMS</ipgapi:CommercialServiceProvider>
         <ipgapi:OrderId>A-b64adf8c-8fe8-44cb-97de-fd721033da2e</ipgapi:OrderId>
         <ipgapi:IpgTransactionId>84566959508</ipgapi:IpgTransactionId>
         <ipgapi:PaymentType>CREDITCARD</ipgapi:PaymentType>
         <ipgapi:ProcessorApprovalCode>403939</ipgapi:ProcessorApprovalCode>
         <ipgapi:ProcessorCCVResponse>M</ipgapi:ProcessorCCVResponse>
         <ipgapi:ProcessorReferenceNumber>119509441809</ipgapi:ProcessorReferenceNumber>
         <ipgapi:ProcessorResponseCode>00</ipgapi:ProcessorResponseCode>
         <ipgapi:ProcessorResponseMessage>Function performed error-free</ipgapi:ProcessorResponseMessage>
         <ipgapi:SchemeTransactionId>0714MCC417474</ipgapi:SchemeTransactionId>
         <ipgapi:TDate>1626255235</ipgapi:TDate>
         <ipgapi:TDateFormatted>2021.07.14 11:33:55 (CEST)</ipgapi:TDateFormatted>
         <ipgapi:TerminalID>80000860</ipgapi:TerminalID>
         <ipgapi:TransactionResult>APPROVED</ipgapi:TransactionResult>
         <ipgapi:TransactionTime>1626255235</ipgapi:TransactionTime>
         </ipgapi:IPGApiOrderResponse>
   </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

In case you have received **SchemeTransactionId** in the response from the Gateway you should use its value in the subsequent RecurringType=REPEAT request:

```

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
                    <ns2:StoreId>1109950006</ns2:StoreId>
                    <ns2:Type>sale</ns2:Type>
                </ns2:CreditCardTxType>
                <ns2:CreditCardData>
                    <ns2:CardNumber>5239*******002</ns2:CardNumber>
                    <ns2:ExpMonth>12</ns2:ExpMonth>
                    <ns2:ExpYear>22</ns2:ExpYear>
                    <ns2:CardCodeValue>XXX</ns2:CardCodeValue>
                </ns2:CreditCardData>
            <ns2:recurringType>REPEAT</ns2:recurringType>
            <ns2:Payment>
                    <ns2:ChargeTotal>13.99</ns2:ChargeTotal>
                    <ns2:Currency>978</ns2:Currency>
                </ns2:Payment>
                <ns2:TransactionDetails>
                     <ns2:ReferencedSchemeTransactionId>0714MCC417474</ns2:ReferencedSchemeTransactionId>
                </ns2:TransactionDetails>
            </ns2:Transaction>
        </ns4:IPGApiOrderRequest>
    </SOAP-ENV:Body>
</SOAP-ENV:Envelope>

```

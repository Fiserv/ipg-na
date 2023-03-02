
# 3-D Secure REST API Integration

## Authentication with the Gateway as 3DS Service provider

The process starts by performing a typical authorization or sale request with a desire to perform 3-D Secure authentication in the request.

The authorization is then placed into a WAITING status until the authentication process is completed. During authentication, the merchant may be required to update the original transaction request one or more times in order to move the process flow forward.

At the end of the authentication process, the original transaction is updated with the authentication results and the authorization is completed.

**Initiate a payment**

Use either the payment card or the payment token to initiate a Primary Payment Transaction.

You can instruct the payment to use 3-D Secure if you want to enforce it. The relevant RequestTypes for 3DSecure authentication are as follows:

- PaymentCardPreAuthTransaction
- PaymentCardSaleTransaction
- PaymentTokenPreAuthTransaction
- PaymentTokenSaleTransaction

This message needs to include the ***authenticationRequest*** object in the transaction request message and includes the following values:

| *Attribute* | *Description*| 
|----|----|
| authenticationType | Default to Secure3D21AuthenticationRequest - this is the default 3DS 2.1 request |
| termURL | Indicates the callback URL where the results of the authentication process should be posted by the ACS server (this is the Access Control Server that executes the cardholder authentication). |
| methodNotifictionURL | If you wish to be notified about the 3DSMethod form display completion, you need to also submit this optional element in your transaction request. The URL should be uniquely identifiable, so when there is a notification received on this URL, you should be able to map it with the corresponding transaction. This eliminates any dependency on the Secure3dTransId which you will receive with the 3DSMethod form response. An easy way to ensure correct transaction mapping is to pass a transaction reference as a query string. For example: "https://www.mywebshop.com/process3dSecureMethodNotificationtransactionReferenceNumber=ffffffff-ba0b-539f-8000-016b2343ad7e" |
| challengeIndicator | In case you would like to influence which authentication flow should be used, you can submit this optional element with one of the values listed below. In case Challenge Indicator is not sent within your transaction request, the Gateway will populate the default value “01” – No preference. |
| challengeWindowSize | If you want to define the size of the challenge window displayed to your customers during the authentication process, you can submit this optional element with one of the values listed below. |

Challenge indicator available values for 3DS protocol version 2.1 are:

- “01” = No preference (You have no preference whether a challenge should be performed. This is the default value)
- “02” = No challenge requested (You prefer that no challenge should be performed.)
- “03” = Challenge requested: 3DS Requestor Preference (You prefer that a challenge should be performed)
- “04” = Challenge requested: Mandate (There are local or regional mandates that mean that a challenge must be performed)

Challenge Window Size values:

- 01 = 250 x 400 
- 02 = 390 x 400 
- 03 = 500 x 600 
- 04 = 600 x 400 
- 05 = Full screen

**Note**: *Based on the payment schemes' observation it is highly recommended to use the value "05 - Full screen" only for browser-based flows. Using full screen mode in app-based flows where the authentication of the cardholder happens on a smartphone or tablet might cause time-outs and trigger an error on issuer/ACS side.*

It is highly recommended to include also Billing and Shipping details in your transaction request to lower the risk of authentication declines. To do this, ensure you populate the objects in any of the sale or preauth requestType payloads.

The following JSON document represents an example of a Sale transaction request with minimal set of elements:

```{r}

{
  "requestType": "PaymentCardSaleTransaction",
    "transactionAmount": {
      "total": "122.04",
      "currency": "USD"
      },
    "paymentMethod": {
      "paymentCard": {
        "number": "403587XXXXXX4977",
        "securityCode": "977",
        "expiryDate": {
        "month": "12",
        "year": "24"
      }   
    }
  },
  “authenticationRequest”: {
    "authenticationType": "Secure3D21AuthenticationRequest",
    "termURL": "https://www.mywebshop.com/process3dSecure",
    "methodNotificationURL": "https://www.mywebshop.com/process3dSecureMethodNotification?transactionReferenceNumber=ffffffff-ba0b-539f-8000-016b2343ad7e",
    "challengeIndicator": "01",
    "challengeWindowSize": "01"
  }
}

```

In case you would prefer to include cardholder's browser parameters directly in the transaction request, you can submit the data in the "cardHolderBrowserParams" attribute:

```{r}

{
   "requestType":"PaymentCardSaleTransaction",
   "transactionAmount":{
      "total":"12.00",
      "currency":"EUR"
   },
   "paymentMethod":{
      "paymentCard":{
         "number":"401699*******0022",
         "securityCode":"XXX",
         "expiryDate":{
            "month":"12",
            "year":"22"
         }
      }
   },
   "authenticationRequest":{
      "authenticationType":"Secure3DAuthenticationRequest",
      "termURL":"https://test.com/webshop/simulator/secure3d/return",
      "methodNotificationURL":"https://test.test/notify",
      "challengeIndicator":"01",
      "cardHolderBrowserParams":{
         "browserAcceptHeaders":"Accept: text/html, application/xhtml+xml, application/xml;q=0.9, image/webp, */*;q=0.8",
         "browserIP":"85.117.56.12",
         "browserLanguage":"es-419",
         "browserColorDepth":"32",
         "browserScreenHeight":"1080",
         "browserScreenWidth":"1920",
         "browserTimeZone":"-300",
         "browserUserAgent":"Lynx/2.8.4rel.1 libwww-FM/2.14 SSL-MM/1.4.1 OpenSSL/0.9.6c"
      }
   }
} 

```

### 3DS Method

If the response from the Gateway contains ‘3DSMethod’ element, it generates hidden iframe, that helps to collect the browser data for the issuers. This information adds to the overall consumer profile and helps in identifying potentially fraudulent transactions.

You need to include the 3DSMethod in your website as hidden iframe. No user interface screen is presented to the cardholder.


The following JSON document represents an example of a response:

```{r}

{
  "clientRequestId": "30dd879c-ee2f-11db-8314-0800200c9a66",
  "apiTraceId": "rrt-0c80a3403e2c2def0-d-ea-28805-6810951-2",
  "ipgTransactionId": "838916029301",
  "transactionType": "SALE",
  "transactionTime": 1518811817,
  "approvedAmount": {
  "total": 122.04,
  "currency": "USD"
},
  "transactionStatus": "WAITING",
  “authenticationResponse”: {
    "type": "3D_SECURE",
    "version": "2.1",
    "secure3dMethod": {
      "methodForm": "&lt;!DOCTYPE iframe SYSTEM "about:legacy-compat"&gt;
      &lt;iframe id="tdsMmethodTgtFrame" name="tdsMmethodTgtFrame"
      style="width: 1px; height: 1px; display: none;" src="javascript:false;"
      xmlns="http://www.w3.org/1999/xhtml"&gt;
      &lt;!--.--&gt; &lt;/iframe&gt;&lt;form id="tdsMmethodForm"
      name="tdsMmethodForm"
      action=https://localhost.modirum.com:8543/dstests/ACSEmu2
      method="post"
      target="tdsMmethodTgtFrame" xmlns="http://www.w3.org/1999/xhtml"&gt;
      &lt;input type="hidden" name="3DSMethodData"
      value="eyAidGhyZWVEU1NlcnZlclRyYW5zSUQiIDogIjAwMDAwMDAwLTU2NzYtNTY2My
      04MDAwLTAwMDAw    &amp;#10;MDAwNDFhOSIsICJ0aHJlZURTTWV0aG9kTm90aWZpY2F0aW9
      uVVJMIiA6ICJodHRwczovL2xvY2Fs&amp;#10;aG9zdC5tb2RpcnVtLmNvbTo4NTQzL21kcGF5bXBpL
      01lcmNoYW50U2VydmVyP21uPVkmdHhpZD0x
      &amp;#10;NjgwOSZkaWdlc3Q9aSUyQnhhUEF5NWFOcVJRbllqNmozbWFDZlFJbTdFdjJYTm
      kwNnh6YmZNJTJG&amp;#10;R3MlM0QiIH0"/&gt; &lt;input type="hidden"
      name="threeDSMethodData"            
      value="eyAidGhyZWVEU1NlcnZlclRyYW5zSUQiIDogIjAwMDAwMDAwLTU2NzYtNTY2
      My04MDAwLTAwMDA
      w&amp;#10;MDAwNDFhOSIsICJ0aHJlZURTTWV0aG9kTm90aWZpY2F0aW9uVVJMIiA
      6ICJodHRwczovL2xvY 2Fs&amp;#10;aG9zdC5tb2RpcnVtLmNvbTo4NTQzL21kcGF5bXBpL01lcm
      NoYW50U2VydmVyP21uPVkmdHhpZD0x&amp;#10;NjgwOSZkaWdlc3Q9aSUyQnhhUEF5NWFOcV
      JRbllqNmozbWFDZlFJbTdFdjJYTmkwNnh6YmZNJTJG&amp;#10;R3MlM0QiIH0"/&gt;
      &lt;/form&gt;&lt;script type="text/javascript" 
      xmlns="http://www.w3.org/1999/xhtml"&gt;
      document.getElementById("tdsMmethodForm").submit(); &lt;/script&gt;",
      "secure3dTransId": "3ac7caa7-aa42-2663-791b-2ac05a542c4a"
    }
  }
}

```

Not all issuers support the collection of browser data using the 3DSMethod Form. In those cases, no data will be posted to the methodNotificationURL, and the flow should continue by posting a status of EXPECTED_BUT_NOT_RECEIVED.

### Frictionless Flow


When a transaction is considered to be a low risk transaction or an exemption is requested, a frictionless flow is applied. In such case the Gateway proceeds with the authorization without additional authentication of the cardholder.

The HTML information is a self-contained HTML block that does not need to be modified or posted, as it will be taken care of automatically when the page in which it is inserted is rendered. Alternatively, this can be created on a page which never becomes visible to you.

If received properly, the response data will be posted to the URL provided in the original methodNotificationURL field and the posted message will contain a threeDSServerTransID field containing the unique transaction id associated with the original request. Note that the payload for this response will contain a single element called threeDSMethodData. That element will contain a base64 encoded JSON response that contains the threeDSServerTransID field.

Example:

```{r}

<form name="frm" method="POST" action="{value from methodNotificationURL}">
<input type="hidden" name="threeDSMethodData" value="eyJ0aHJlZURTU2VydmVyVHJhbnNJRCI6IjNhYzdjYWE3LWFhNDItMjY2My03OTFiLTJhYzA1YTU0MmM0YSJ9">
</form>

```

You should wait a minimum of 10 seconds for the above POST operation to complete and then you need to notify the Gateway, that the authentication process can continue by submitting the methodNotificationStatus with the values based on corresponding conditions: 

**RECEIVED** = in case you have submitted the element methodNotificationURL in the initial Sale transaction request and have received the notification from ACS within 10 seconds, you will receive HTTP POST message from ACS, which will contain  a unique transaction identifier represented by secure3DTransID
**EXPECTED_BUT_NOT_RECEIVED** = in case you have submitted the element methodNotificationURL in the initial Sale transaction request and have not received the notification from ACS within 10 seconds
**NOT_EXPECTED** = in case you have NOT submitted the element methodNotificationURL in the initial Sale transaction request

This is done by performing a PATCH operation on the original transaction. 
The following JSON document represents an example of a request to be sent after 3DSMethod form display:

```{r}

{
  "authenticationType": "Secure3D21AuthenticationUpdateRequest",
  "storeId": "12345500000",
},
    "methodNotificationStatus": "RECEIVED"
}

```

The following JSON document represents an example of a response you receive from the API indicating, that the authentication has been successful, and authorization approved:

```{r}

{
  "clientRequestId": "30dd879c-ee2f-11db-8314-0800200c9a66",
  "apiTraceId": "rrt-0c80a3403e2c2def0-d-ea-28805-6810951-2",
  "ipgTransactionId": "838916029301",
  "transactionType": "SALE",
  "transactionTime": 1518811817,
  "approvedAmount": {
    "total": 122.04,
    "currency": "USD"
    },
  "transactionStatus": "APPROVED",
  "schemeTransactionId": "019078743804756",
  "processor": {
    "responseCode": "00",
    "responseMessage": "APPROVED",
    "authorizationCode": "OK7118"
    },
    "secure3dResponse": {
      "responseCode3dSecure": "1"
    }
  }
}

```

### Challenge Flow

This flow is triggered, when the transaction is not considered as low risk or in case the issuer requires additional authentication of the cardholder. The whole process starts with initial Sale transaction request as described above in section "Frictionless Flow" until the step where 3DS Method is displayed. 

Once the 3DS Method call has been completed, you need to notify the Gateway that the authentication process can continue by submitting **methodNotificationStatus** element with the values based on corresponding conditions from the 3DSecure Method Form above. This is done by performing a PATCH operation on the original transaction.

**RECEIVED** = in case you have submitted the element methodNotificationURL in the initial Sale transaction request and have received the notification from ACS within 10 seconds, you will receive HTTP POST message from ACS, which will contain  a unique transaction identifier represented by secure3DTransID
**EXPECTED_BUT_NOT_RECEIVED** = in case you have submitted the element methodNotificationURL in the initial Sale transaction request and have not received the notification from ACS within 10 seconds
**NOT_EXPECTED** = in case you have NOT submitted the element methodNotificationURL in the initial Sale transaction request

The following JSON document represents an example of a request to be sent after 3DSMethod form display:

```{r}

{
  "authenticationType": "Secure3D21AuthenticationUpdateRequest",
  "storeId": "12345500000",
},
  "methodNotificationStatus": "RECEIVED"
}

```

Our Gateway verifies the response and provides the result back to you, including the challenge result data:

```{r}

{
  "clientRequestId": "30dd879c-ee2f-11db-8314-0800200c9a66",
  "apiTraceId": "rrt-0c80a3403e2c2def0-d-ea-28805-6810951-2",
  "ipgTransactionId": "838916029301",
  "transactionType": "SALE",
  "transactionTime": 1518811817,
  "approvedAmount": {
  "total": 122.04,
  "currency": "USD"
},
  "transactionStatus": "WAITING",
  "authenticationResponse": {
    "type": "3D_SECURE",
    "version": "2.1",
    "params": {
      "acsURL": "https://3ds-acs.test.modirum.com/mdpayacs/pareq",
      "termURL": "https://www.mywebshop.com/process3dSecure/",
      "cReq": "ewogICAiYWNzVHJhbCIgOiA...wMDAtMDAwMDAwMDA0MWE5Igp9",
      "sessiondata": "50F2156E03083CA665BCB4.."
      }
    }
  }
}

```

The response will contain an authenticationResponse object with the following fields:

| *Field* | *Description* |
|----|----|
| type | 3D_SECURE |
| version | 2.1.0 |
| acsURL | The URL to which the cReq and sessionData values should be posted for the cardholder challenge to take place |
| termURL | The URL where the results of the authentication will be posted |
| cReq | An encoded request message returned from the ACS server |
| sessionData | An encoded list of session parameters to be used for authentication. Please note, that this value may not always be provided |


In the next step you need to POST the data to the indicated URL usually implemented as auto-submit form. This needs to be implemented within your website. We recommend you to POST the challenge request element without capitals (e.g. ‘creq’) to avoid any problems in a communication with the ACS.

The cardholders will be redirected to the ACS and presented with the UI to collect the authentication details - for example enter one-time-password or perform authentication using their banking app (out-of-band authentication). After authentication completion the consumer is redirected back to your webpage.

```{r}

<form name="frm" method="POST" action="https://3ds-acs.test.modirum.com/mdpayacs/pareq ">
  <input type=”hidden” name=”creq” value=”ewogICAiYWNzVHJhbCIgOiA...wMDAtMDAwMDAwMDA0MWE5Igp9”>
  <input type=”hidden” name=”threeDSSessionData” value=”50F2156E03083CA665BCB4..”>
</form>

```

When the authentication is completed, an authentication response will be posted to the URL specified in ***termURL*** field.

**Request to complete the transaction**

After you received the data from the ACS, you need to submit them to the Gateway in cRes element together with the reference to the original transaction. This is done by sending PATCH request to the original transaction and includes the following values:

| *Field* | *Description* |
|----|----|
| authenticationType | Secure3D21AuthenticationUpdateRequest |
| acsResponse/cRes | The cRes data posted to the termURL by the ACS server |

The following JSON document represents an example of a request with cRes element:

{
  "authenticationType": "Secure3D21AuthenticationUpdateRequest",
  "storeId": "12345500000",
  "billingAddress": {
    "company": "Test Company",
    "address1": "5565 Glenridge Conn",
    "address2": "Suite 123"
    "city": "Atlanta",
    "region": "Georgia",
    "postalCode": "30342",
    "country": "USA"
  },
  "securityCode": "123",
  "acsResponse": {
    "cRes": "ewogICAiYWNzUmVmZX…Fuc1N0YXR…IKfQ=="
  }
}

The following JSON document represents an example of a response you receive from the Gateway indicating, that the authorization has been successful:

```{r}

{
  "clientRequestId": "30dd879c-ee2f-11db-8314-0800200c9a66",
  "apiTraceId": "rrt-0c80a3403e2c2def0-d-ea-28805-6810951-2",
  "ipgTransactionId": "838916029301",
  "transactionType": "SALE",
  "transactionTime": 1518811817,
  "approvedAmount": {
    "total": 122.04,
    "currency": "USD"
  },
  "transactionStatus": "APPROVED",
  "schemeTransactionId": "019078743804756",
  "processor": {
    "responseCode": "00",
    "responseMessage": "APPROVED",
    "authorizationCode": "OK7118"
  },
  "secure3dResponse": {
    "responseCode3dSecure": "1"
  }
}

```

### Fallback to 3DS protocol 1.0

For cases, where the issuers do not support EMV 3DS protocol yet, the Gateway provides an option to “downgrade” to 3DS 1.0 authentication instead.

In the first step you need to POST an API request as for EMV 3DS protocol:

```{r}

{
  "requestType": "PaymentCardSaleTransaction",
    "transactionAmount": {
      "total": "12.99",
      "currency": "EUR"
      },
    "paymentMethod": {
      "paymentCard": {
        "number": "403587XXXXXX4977",
        "securityCode": "999",
        "expiryDate": {
        "month": "12",
        "year": "24"
      }  
    }
  },
  "authenticationRequest": {
    "authenticationType": "Secure3D21AuthenticationRequest",
    "termURL": "https://test.ipg-online.com/webshop/simulator/secure3d/return",
    "methodNotificationURL": "https://test.ipg-online.com/ipgconfirmation/services/secure3ds",
    "challengeIndicator": "01",
    "challengeWindowSize": "01"
  }
}

```

You will receive a response from the Gateway indicating, that credit card is enrolled for 3DS version 1 only:

```{r}

{
   "clientRequestId": "55351544-749a-4c03-9e35-3e240ea5572d",
   "apiTraceId": "YKUh6bqtrBfPwvICng2wBgAAATM",
   "ipgTransactionId": "84563547902",
   "orderId": "R-ff489e2d-b5f3-4757-a91b-0a774681e26a",
   "transactionType": "SALE",
   "transactionOrigin": "ECOM",
   "paymentMethodDetails":    {
      "paymentCard":       {
         "expiryDate":          {
            "month": "12",
            "year": "2024"
         },
         "bin": "403587",
         "last4": "4977",
         "brand": "VISA"
      },
      "paymentMethodType": "PAYMENT_CARD"
   },
   "country": "Germany",
   "transactionTime": 1621434858,
   "transactionStatus": "WAITING",
   "authenticationResponse":    {
      "type": "3D_SECURE",
      "version": "1.0",
      "params":       {
         "payerAuthenticationRequest": "eJxVUdtygjAQ/RXG184QEvASZ80M1V54aAcRP4BCWqgSNAlW/r4JeGn3ac/Jnt3NWUhLyflqw/NWcgZvX
KnsiztVsRjFyXo88Yg3xSMGcZjwI4MTl6pqBMOu5xJAV2h0Mi8zoRlk+fExemfjPgBdINRcRitGqWfCBzRAEFnNWRS/OClX2vFXG0A9BXnTCi07NiM
TQFcArdyzUuuDmiOkjcL1C+V+VlLpItOZmzc1IFsD6L5P3NpMmZ7nqmBxkW4flj80weK7DE9h130872b7VES7BSBbAaYVZ8Qj2Btj6uBg7gdzPAP
U85DVdhn2tE0cTFxKzQ8HBg52UDgATOzLXwaMv5KLvGN0aprdEPDzoRHcVBg7bzmg+9rLV2tqro1f2Pc96uMAW197xsorYw0J8KC3AJDVoM
vJ0OWmJvt361+B66YO",
         "termURL": "https://test.ipg-online.com/webshop/simulator/secure3d/return",
         "merchantData": "",
         "acsURL": "https://3ds-acs.test.modirum.com/mdpayacs/pareq"
      }
   }
}

```

In the next step you need to POST the data to the indicated URL usually implemented as auto-submit form. This needs to be implemented within your website. We recommend you to POST the challenge request element without capitals (e.g. ‘pareq’) to avoid any problems in a communication with the ACS.
The cardholders will be redirected to the ACS and presented with the UI to collect the authentication details - for example enter one-time-password or perform authentication using their banking app (out-of-band authentication). After authentication completion the consumer is redirected back to your webpage.

```{r}

<form name="frm" method="POST" action="https://3ds-acs.test.modirum.com/mdpayacs/pareq ">
  <input type=”hidden” name=”pareq” value=”ewogICAiYWNzVHJhbCIgOiA...wMDAtMDAwMDAwMDA0MWE5Igp9”>
  <input type=”hidden” name=”threeDSSessionData” value=”50F2156E03083CA665BCB4..”>
</form>

```

After you received the data from the ACS, you need to submit them to the Gateway in “payerAuthenticationResponse” element together with the reference to the original transaction. This is done by sending PATCH request to the original transaction.

**Note**: The element “merchantData” might not be returned by all issuers, in case you have not received it in  previous step, please do not submit in the next PATCH request

PATCH */ipgrestapi/v2/services/payments/{ipgTransactionId}*

```{r}

{
  "authenticationType": "Secure3D10AuthenticationUpdateRequest",
  "billingAddress": {
    "address1": "5565 Glenridge Conn",
    "city": "Atlanta",
    "postalCode": 30342,
    "country": "USA"
  },
  "merchantData": "MD____13992017033012241629.....c-4a40-aeb4-b41a8a34480fa067ac",
  "payerAuthenticationResponse": "eJzlWFeP67iS/………9Xm88X5c/37Pcj6I/v3P8JV86aGw=="
}

```

The following JSON document represents an example of a response you receive from the Gateway indicating, that the authorization has been successful and flagged as authenticated.

```{r}

{
   "clientRequestId": "4c3aa885-db8e-43fb-b3c4-0e5c6927408c",
   "apiTraceId": "YKUjRJVBbdinNESL8Era8AAAAIs",
   "ipgTransactionId": "84563547902",
   "orderId": "R-ff489e2d-b5f3-4757-a91b-0a774681e26a",
   "transactionType": "SALE",
   "transactionOrigin": "ECOM",
   "paymentMethodDetails":    {
      "paymentCard":       {
         "expiryDate":          {
            "month": "12",
            "year": "2024"
         },
         "bin": "403587",
         "last4": "4977",
         "brand": "VISA"
      },
      "paymentMethodType": "PAYMENT_CARD"
   },
   "country": "Germany",
   "terminalId": "80000860",
   "merchantId": "000102072004393",
   "transactionTime": 1621434858,
   "approvedAmount":    {
      "total": 12.99,
      "currency": "EUR",
      "components": {"subtotal": 12.99}
   },
   "transactionStatus": "APPROVED",
   "secure3dResponse": {"responseCode3dSecure": "1"},
   "schemeTransactionId": "519154004377788",
   "processor":    {
      "referenceNumber": "113914232351",
      "authorizationCode": "907587",
      "responseCode": "00",
      "responseMessage": "Function performed error-free",
      "avsResponse":       {
         "streetMatch": "N",
         "postalCodeMatch": "N"
      }
   }
}

```

### Authentication with external 3DS Service provider

In case you are using your own / external 3DS Service provider and plan to send authorization request to the Gateway, you need to submit the authentication values obtained from your 3DS service provider.

| *Field* | *Description* |
|----|----|
| authenticationType | Used for submitting authentication result performed by an external 3-D Secure service provide |
| cavv | Authentication value obtained in the authentication response from external 3-D Secure service provider |
| dsTransactionId | Authentication transaction reference ID, obtained from external 3-D Secure provider |
| authenticationResponse | Represents the result of the authentication, allowed enum values: <br/>  Y = fully authenticated request <br/>  A = successful authentication attempt  <br/> Please note, that any different values provided in the request will be automatically declined by the Gateway.|

The following JSON document represents an example of a sale transaction submitted to our Gateway after being fully authenticated by an external service provider:

```{r}

{
  "requestType": "PaymentCardSaleTransaction",
  "transactionAmount": {
               "total": "12.00",
               "currency": "EUR"
  },
  "paymentMethod": {
               "paymentCard": {
                               "number": "401699XXXX0006",
                               "securityCode": "999",
                               "expiryDate": {
                                   "month": "12",
                                   "year": "24"
                               }
               }
  },
  "authenticationResult": {
      "authenticationType": "Secure3DAuthenticationResult",
      "cavv": "AAAAAAAAAAAAAAAAAAAAAAAAAAA=",
      "dsTransactionId": "5a56fdc9-6d47-5fee-8000-000000296743",
      "authenticationResponse": "Y"
   }
}

```

The following JSON document represents an example of a response you receive from the Gateway indicating, that the authorization has been successful and flagged as authenticated:

```{r}

{
   "clientRequestId": "97c67e8f-7c2d-421d-9d97-b749206aab06",
   "apiTraceId": "YJPLezoO2XZa9K8QL10bvgAAA98",
   "ipgTransactionId": "84411977859",
   "orderId": "R-941fc643-adae-4468-bc48-26e5099f4367",
   "transactionType": "SALE",
   "transactionOrigin": "ECOM",
   "paymentMethodDetails":    {
      "paymentCard":       {
         "expiryDate":          {
            "month": "12",
            "year": "2024"
         },
         "bin": "401699",
         "last4": "0006",
         "brand": "VISA"
      },
      "paymentMethodType": "PAYMENT_CARD"
   },
   "country": "USA",
   "terminalId": "80000012",
   "merchantId": "520334507229862",
   "transactionTime": 1620298619,
   "approvedAmount":    {
      "total": 12,
      "currency": "EUR",
      "components": {"subtotal": 12}
   },
   "transactionStatus": "APPROVED",
   "secure3dResponse": {"responseCode3dSecure": "1"},
   "schemeTransactionId": "234567891234560",
   "processor":    {
      "referenceNumber": "112610940537",
      "authorizationCode": "005042",
      "responseCode": "00",
      "responseMessage": "Function performed error-free",
      "avsResponse":       {
         "streetMatch": "Y",
         "postalCodeMatch": "Y"
      },
      "securityCodeResponse": "MATCHED"
   }
}

```

> [Back to 3-D Secure main page](?path=docs/3dsecure-md/3DSecure.md)



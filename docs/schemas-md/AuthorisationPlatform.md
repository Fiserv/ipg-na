
# Nashville Response Codes


## COMMON RESPONSE CODES


**GENERAL CREDIT / DEBIT CARD PROCESSING**

| *Code*   | *Description*| *IPG  Approval Code* |
|----|----|----|
| 00 | Transaction has been approved. | Y:000000:3989951798:PPX:259280509 |
| 05 | The credit card being used for the transaction has been rejected by the issuer. | N:05:Do Not Honour |
| 5002 | The merchant does not have a service entry for the credit card brand within the transaction request.	 | N:-5002:brand not supported |
| 5993 | The transaction has been cancelled by the user. | N:-5993:Cancelled by user |
| 12000 | The merchant is configured for mandatory card code but sent a transaction without a card code value. | N:-12000:Card security code is mandatory |

**CONFIGURATION ISSUES**

| *Code*   | *Description*| *IPG  Approval Code* |
|----|----|----|
| 5002 | The merchant does not have a service entry for the credit card brand within the transaction request. | N:-5002:brand not supported |
| 30053 | The transaction timed out. | N:-30053:Communication Error |
| 30053 | Exception occurred retrieving the message from the endpoint. |N:-30053:Communication Error |
| 30060 | An error occured building, parsing or interpreting the message. | N:30060:Internal Error |
| 50653 | Incorrect currency has been sent in the request. | N:-50653:Sent invalid currency or no currencies were setup for this store |

# ADDITIONAL RESPONSE CODES

## AUTHORIZATION DECLINES (NASHVILLE FRONT-END)

| *Code*   | *Description*|
|----|----|
| 01 | Refer to issuer |
| 03 | Invalid merchant |
| 12 | Invalid transaction |
| 13 | Invalid amount |
| 14 | Invalid card number |
| 25 | Invalid terminal	|
| 28 | Please retry	|
| 51 | Declined |
| 54 | Wrong expiration/expired card |
| 55 | Incorrect PIN |
| 57 | Invalid txn for card	|
| 60 | Declined |
| 61 | Exceeds withdrawal limit |
| 63 | Service not allowed |
| 69 | Host key error |
| 75 | PIN try exceeded	|
| 89 | Invalid Terminal ID |
| 91 | System error	|
| 94 | Duplicate transaction |
| 1A | Add Auth Require	 |
| C2 | CVV2 Declined |
| RW | Rev Outside Win |


##GATEWAY DECLINES


| *Code*   | *Description*|
|----|----|
| 100 | Internal error	 |
| 2303 | Invalid credit card number|
| 2304 | Credit card is expired or expiration date is invalid |
| 5004 | The order does not include an authorized preauth	 |
| 5005 | Blocked due to fraud prevention setting	 |
| 5006 | Transaction to be voided was not found	|
| 5007 |Amount within void transaction is invalid - please omit or correct	|
| 5009 | No transaction found in order which can be returned	 |
| 5017 | Voiding of returned transactions is not supported	 |
| 5018 | No transaction found for void	 |
| 5019 | The transaction to be voided is not voidable	|
| 5022 | The preauth is not voidable as long as there is a captured postauth - please void the postauth before	 |
| 5100 | Invalid 3D Secure response value combination	|
| 5101 | Transaction declined. 3D Secure authentication failed.	|
| 5102 | Transaction failed. ECI-7 transactions are not supported by merchant.	 |
| 5103 | used for 3DSecure waiting to declined	|
| 5108 | Transaction failed. MOTO transaction are not supported in Connect.	 |
| 5111 | Transaction failed. ECI1 and ECI6 transactions are not supported by merchant.	|
| 5112 | Transaction failed. Debit card not authenticated.	|
| 5115 | Transaction failed	|
| 5433 | Merchant setup incorrectly	 |
| 5995 | order too old to be referenced	 |
| 5996 | Brand / card type is invalid or not supported	 |
| 5998 | Other transaction with same order id currently being processed	 |
| 7778 | Transaction timed out and has not been processed, please retry	 |
| 10421 | The merchant is not setup to support split shipment	 |
| 10422 | No further PostAuth possible for this Order ID	 |
| 10423 | No final shipment settled yet	 |
| 10424 | No further PostAuth possible for this Order ID	 |
| 10425 | Missing mandatory split shipment information	 |
| 10426 | Split shipment not allowed since the previous postauth is non split shipment.	 |
| 10501 | Only approved (and not yet captured) PreAuth transactions can be captured by a PostAuth.	 |
| 10501 | PostAuth already performed	 |
| 10503 | Invalid amount or currency	 |
| 10504 | This return is not voidable	 |
| 12000 | Card security code is mandatory	 |
| 13532 | Invalid card type	 |
| 20429 | The merchant is not setup to support cashback	 |
| 20430 | Transaction type not supported for cashback	 |
| 20431 | Payment type not supported for cashback	 |
| 21281 | The merchant is not setup to support airline	 |
| 22812 | Different currencies in the order	 |
| 22813 | Currency is not allowed, because approved transactions on the same order have another currency	 |
| 23032 | transaction origin type MOTO/RETAIL not supported for MCC7995 payment of gaming winnings	 |
| 28319 |RuPay authentication error	  |
| 30050 | Transaction timed out	 |
| 30052 | Transaction timed out	 |
| 30053 | Transaction timed out	 |
| 30055 | Not configured for 3DSecure	 |
| 30054 | Transaction timed out	 |
| 30062 |Transaction timed out	  |
| 30157 | The merchant is not setup to support the requested service.	 |
| 30158 | Missing approval code for offline transaction.	 |
| 30159 | This transaction was recieved as declined from point of sale	 |
| 31218 | The merchant is not setup to support the requested service	 |
| 31319 | The merchant is not setup to support contract ID for insurance service.	 |
| 42217 |  invalid MCC configured for hotel lodging merhant, MCC must be 3501-3999 or 7011	 |
| 42218 | The merchant is not setup to support hotel lodging	 |
| 42317 |  invalid MCC configured for car rental merhant, MCC must be 3351-3500, 7512, 7513 or 7519	 |
| 42318 | The merchant is not setup to support car rental|
| 42741 | Invalid IBAN or Credit card number	 |
| 42742 | Recurring type not supported to be set in the transaction	 |
| 42744 | Internal error	 |
| 42745 | Internal error	 |
| 42754 | Only Ecommerce sale or refunds are supported	 |
| 42755 |3DSecure Transaction Not Authenticated	  |
| 50002 | 3d secure data validation error AAV/CAVV	 |
| 50003 | 3d secure data validation error XID-ECI	 |
| 50294 |Wrong card information sent	  |
| 50295 | The preauth is not voidable as long as there is an authorised incremental preauth - please void the incremental preauth before	 |
| 50305 | Referenced transaction is not in the correct transaction state	 |
| 50306 | Unable to get PARes	 |
| 50307 | Empty PARes in response	 |
| 50308 |  Wrong transaction state	 |
| 50655 | Unable to verify card enrollment	 |
| 50656 | Declined by Fraud Detect	 |
| 50666 | Account owner name not provided	 |
| 50715 | Referenced transaction is either not found or not in proper status to process subsequent 3DS Method request	 |
| 50734 | Non Payment Authentication passthrough transaction should have zero amount.	 |
| 50735 | Non Payment Authentication passthrough transaction should be a Preauth.	 |
| 50736 | For 3DSecure EMVCO Message Type NPA a subsequent sale transaction is not allowed!	 |
| 50677 | Unable to convert to VOID transaction	 |
| 50678 | Payer authentication error	 |
| 50681 |  Missing data in payer authentication response	 |
| 50682 |Missing merchant data in payer authentication response	  |
| 50683 |  Missing secure 3D data	 |
| 50687 |Split Authentication transactions not supported	  |
| 50688 | Store doesn't support MPI via API	 |
| 50690 | Declined by Fraud Detect	 |
| 50698 | The transaction type of the referenced transaction is incompatible with the current transaction	 |
| 50715 | Referenced transaction not found	 |
| 50716 | Transaction declined. 3D Secure authentication failed.	 |
| 59365 | Unable to save emv response data into database	 |
| 59366 | Reference number missing	 |
| 62086 | Setup Error	 |
| 63096 | Setup Error	 |


| *HTTP RESPONSE*   | *Scheme Response*| *Example Response Payload* |
|----|----|----|
| 400 | Review ErrorResponse under Schemas  - https://docs.firstdata.com/org/gateway/docs/api#models |  { <br/>  "clientRequestId": "8061887",<br/>  "responseType": "badRequest",<br/> "error": {<br/>"code": "400",<br/> "message": "Bad Request" <br/>} <br/>} |
| 401 | Review ErrorResponse under Schemas  - https://docs.firstdata.com/org/gateway/docs/api#models | { "clientRequestId": "8487567", "responseType": "Unauthenticated", "error": {"code": "401", "message": "Invalid API key" } } |
| 403 | Review ErrorResponse under Schemas  - https://docs.firstdata.com/org/gateway/docs/api#models | { "responseType": "Unauthorized", "error": { "code": "403",  "message": "Not authorized to access the resource" }} |
| 409 | Review TransactionErrorResponse under Schemas  - https://docs.firstdata.com/org/gateway/docs/api#models | {"clientRequestId": "822985",  "apiTraceId": "rrt-0ec057ce9d392353e-d-ea-20546-32667622-1",  "responseType": "GatewayDeclined","orderId": "R-65901845-a377-47e5-8426-dd6f4b200dfc", "transactionTime": 1584473727, "transactionStatus": "VALIDATION_FAILED",  "error": {  "code": "5002",  "message": "The merchant is not setup to support hosted data"  }} |
| 415 | Review ErrorResponse under Schemas  - https://docs.firstdata.com/org/gateway/docs/api#models | { "clientRequestId":"8043822", "apiTraceId":"rrt-0376b5dad157b2f74-c-ea-20368-32171256-1", "error": { "code":"415",  "message":"Unsupported Media Type"  }} |
| 422 | Review TransactionErrorResponse under Schemas  - https://docs.firstdata.com/org/gateway/docs/api#models |{<br/>     "clientRequestId": "8190936",<br/>  "apiTraceId": "rrt-01550643f01a14a4e-b-ea-20474-44842749-1",<br/> "responseType": "EndpointDeclined",<br/>  "ipgTransactionId": "84532745762",<br/>  "orderId": "R-0552c865-091d-40a2-a7bd-cb1408e2b23e",<br/>  "transactionType": "PREAUTH", <br/> "transactionOrigin": "ECOM",<br/>    "paymentMethodDetails": {<br/>  "paymentCard": {<br/>   "expiryDate": {<br/>  "month": "12",<br/> "year": "2025"<br/> },<br/> "bin": "373953",<br/> "last4": "1004",<br/>           "brand": "AMEX"        },<br/>  "paymentMethodType": "PAYMENT_CARD"<br/> },<br/>  "country": "USA",<br/> "terminalId": "1234567",<br/> "merchantId": "541581429648",<br/> "transactionTime": 1585311765,<br/>  "transactionStatus": "DECLINED",<br/>  "schemeTransactionId": "010087922579065",<br/>   "processor": {    "referenceNumber": "84532745762 ",<br/> "responseCode": "51",<br/>   "network": "AMEX",<br/>  "associationResponseCode": "100",<br/>  "responseMessage": "DECLINED",<br/>   "avsResponse": {<br/> "streetMatch": "N",<br/> "postalCodeMatch": "N"<br/>        },        "securityCodeResponse": "NOT_PROCESSED"<br/>   }<br/>}  |
| 500 | Review BasicResponse under Schemas  - https://docs.firstdata.com/org/gateway/docs/api#models | {<br/>  "clientRequestId":"6435754",{<br/>  "apiTraceId":"rrt-0376b5dad157b2f74-c-ea-20368-32176218-1",{<br/>  "responseType":"ServerError"<br/>} |








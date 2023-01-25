
# TransactionResponse

| *description*:   | *Transaction response with error field included*.|
|----|----|
| clientRequestId |    ``` string ```  *example:   30dd879c-ee2f-11db-8314-0800200c9a66*. Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7*. Request identifier in API, can be used to request logs from the support team.|
| responseType | ResponseType   ``` string ```  *example: Unauthenticated*. The type of the response. Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| ipgTransactionId |    ``` string ```  *example: 838916029301*. The response transaction ID.|
| orderId |    ``` string ```  *example: 123456*. Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| transactionType | TransactionType   ``` string ```  *example: SALE*. Type of transaction to perform. Primary transaction types in requests include 'SALE', 'PREAUTH', 'CREDIT' and 'FORCED_TICKET'. Enum:    > Array [ 9 ] - [ SALE, PREAUTH, CREDIT, FORCED_TICKET, VOID, RETURN, POSTAUTH, PAYER_AUTH, DISBURSEMENT ]|
| paymentToken | |
| transactionOrigin | TransactionOrigin   ``` string ```  *example: ECOM*. The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| paymentMethodDetails | |
| country |    ``` string ```  *example: USA*. Country of the card issuer.|
| terminalId | ResponseType   ``` string ```  *maxLength: 30  example: 123456*. The terminal that is processing the transaction.|
| merchantId | ResponseType   ``` string ```  *example: 199950008*. The unique (on Acquirer level) mechant ID. Usually this value has been chosen from the merchant itself and will be used in communication with the endpoint.|
| merchantTransactionId |    ``` string ```  *maxLength: 40  example: lsk23532djljff3*. The unique merchant transaction ID from the request header, if supplied.|
| transactionTime |    ``` integer ```  *example: 1518811817*. The transaction time in seconds since epoch.|
| approvedAmount | |
| transactionStatus |    ``` string ```  *example: APPROVED*. Represents the status of a transaction immediately following the original processing request. This value is not stored for the transaction and is only available in the response when the transaction is processed. TransactionStatus is not returned on either the transaction inquiry or on the order inquiry. Enum:Array [ 6 ] - [ APPROVED, WAITING, PARTIAL, VALIDATION_FAILED, PROCESSING_FAILED, DECLINED ]|
| approvalCode |    ``` string ```  *example: N:-30031:No terminal setup*. Shows the transaction approvalcode.|
| errorMessage |    ``` string ```  *example: 000100: Tx was processed but response was not stored correctly*. Shows the transaction errorMessage.|
| transactionState |    ``` string ```  *example: AUTHORIZED*. Shows the state of the current transaction.Enum:Array [ 12 ] - [ AUTHORIZED, CAPTURED, DECLINED, CHECKED, COMPLETED_GET, INITIALIZED, PENDING, READY, TEMPLATE, SETTLED, VOIDED, WAITING ]|
| approvalCode |    ``` string ```  *example: N:-30031:No terminal setup*. Shows the transaction approvalcode.|
| errorMessage |    ``` string ```  *example: 000100: Tx was processed but response was not stored correctly*. Shows the transaction errorMessage.|
| transactionState | ResponseType   ``` string ```  *example: AUTHORIZED*. Shows the state of the current transaction. Enum:Array [ 12 ] - [ AUTHORIZED, CAPTURED, DECLINED, CHECKED, COMPLETED_GET, INITIALIZED, PENDING, READY, TEMPLATE, SETTLED, VOIDED, WAITING ]|
| paymentAccountReferenceNumber |    ``` string ```  *maxLength: 30  example: 1234001AB101112131415161718CV*. Payment Account Reference Number from response, if supplied.|
| secure3dResponse |   |
| standinResponseDetails |   |
| redirectURL |    ``` string ```  *example:  `http://pay.issuer-bank.com/sessionID=123&sharedKey=456`*. The endpoint redirection URL.|
| authenticationResponse |   |
| schemeTransactionId |    ``` string ```  *maxLength: 40  example: 019078743804756*. The transaction ID received from schemes for the initial transaction of card on file flows.|
| processor |   |
| additionalDetails |   |
| accountUpdaterResponse |   |
| achResponse |   |
| currencyConversionResponse |   |
| requiredActions |   |
| plannedDueDate |    ``` string ```  *pattern: ^\d{4}-(0[1-9]P1[0-2])-(0[1-9]P[12][0-9]P3[01])$  example: 2022-03-03*. Capture PlannedDueDate field sent for SEPA transactions.|
| networkToken |   |
| error | |  




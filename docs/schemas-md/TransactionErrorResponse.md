
# TransactionErrorResponse

| *description*:   | *Transaction response with error field included*.|
|----|----|
| clientRequestId |    ``` string ```   <br/> *example:   30dd879c-ee2f-11db-8314-0800200c9a66* <br/>  Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  <br/> *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7* <br/> Request identifier in API, can be used to request logs from the support team.|
| responseType | ResponseType   ``` string ``` <br/>  *example: Unauthenticated*.  <br/> The type of the response.  <br/> Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| ipgTransactionId |    ``` string ```   <br/> *example: 838916029301* <br/>  The response transaction ID.|
| orderId |    ``` string ```  <br/>  *example: 123456* <br/>  Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| transactionType | TransactionType   <br/>  ``` string ```  <br/>  *example: SALE* <br/>  Type of transaction to perform. Primary transaction types in requests include 'SALE', 'PREAUTH', 'CREDIT' and 'FORCED_TICKET'.  <br/> Enum:    > Array [ 9 ] - [ SALE, PREAUTH, CREDIT, FORCED_TICKET, VOID, RETURN, POSTAUTH, PAYER_AUTH, DISBURSEMENT ]|
| paymentToken |    ``` integer ``` <br/>  ($int64)  <br/>   *example: Germany* <br/>  Country of the card issued.|
| transactionOrigin | [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md)  <br/>   ``` string ```  <br/>  *example: ECOM*.  <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| paymentMethodDetails | [PaymentMethodDetails](?path=docs/schemas-md/PaymentMethodDetails.md)|
| country |    ``` string ```  <br/>  *example: USA* <br/>  Country of the card issuer.|
| terminalId | ResponseType   ``` string ```   <br/> *maxLength: 30   <br/> example: 123456* <br/>  The terminal that is processing the transaction.|
| merchantId | ResponseType   ``` string ```  <br/> *example: 199950008* <br/>  The unique (on Acquirer level) mechant ID. Usually this value has been chosen from the merchant itself and will be used in communication with the endpoint.|
| merchantTransactionId |    ``` string ```   <br/> *maxLength: 40   <br/> example: lsk23532djljff3* <br/>  The unique merchant transaction ID from the request header, if supplied.|
| transactionTime |    ``` integer ```   <br/> *example: 1518811817* <br/>  The transaction time in seconds since epoch.|
| approvedAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| transactionStatus |    ``` string ```  <br/> *example: APPROVED* <br/> Represents the status of a transaction immediately following the original processing request. This value is not stored for the transaction and is only available in the response when the transaction is processed. TransactionStatus is not returned on either the transaction inquiry or on the order inquiry. Enum:Array [ 6 ] - [ APPROVED, WAITING, PARTIAL, VALIDATION_FAILED, PROCESSING_FAILED, DECLINED ]|
| approvalCode |    ``` string ```  <br/>  *example: N:-30031:No terminal setup* <br/> Shows the transaction approvalcode.|
| errorMessage |    ``` string ```  <br/>  *example: 000100: Tx was processed but response was not stored correctly* <br/>  Shows the transaction errorMessage.|
| transactionState |    ``` string ``` <br/>   *example: AUTHORIZED* <br/> Shows the state of the current transaction. <br/> Enum:Array [ 12 ] - [ AUTHORIZED, CAPTURED, DECLINED, CHECKED, COMPLETED_GET, INITIALIZED, PENDING, READY, TEMPLATE, SETTLED, VOIDED, WAITING ]|
| approvalCode |    ``` string ```  <br/>  *example: N:-30031:No terminal setup* <br/>  Shows the transaction approvalcode.|
| errorMessage |    ``` string ```   <br/> *example: 000100: Tx was processed but response was not stored correctly* <br/> Shows the transaction errorMessage.|
| transactionState | ResponseType   ``` string ```  <br/>  *example: AUTHORIZED* <br/>  Shows the state of the current transaction.  <br/> Enum:Array [ 12 ] - [ AUTHORIZED, CAPTURED, DECLINED, CHECKED, COMPLETED_GET, INITIALIZED, PENDING, READY, TEMPLATE, SETTLED, VOIDED, WAITING ]|
| paymentAccountReferenceNumber |    ``` string ```   <br/> *maxLength: 30  <br/>  example: 1234001AB101112131415161718CV* <br/> Payment Account Reference Number from response, if supplied.|
| secure3dResponse |  [Secure3dResponse](?path=docs/schemas-md/Secure3dResponse.md)|
| standinResponseDetails |  [StandinResponseDetails](?path=docs/schemas-md/StandinResponseDetails.md)|
| redirectURL |    ``` string ```   <br/> *example:  `http://pay.issuer-bank.com/sessionID=123&sharedKey=456`* <br/> The endpoint redirection URL.|
| authenticationResponse | [Secure3DAuthenticationResponse](?path=docs/schemas-md/Secure3DAuthenticationResponse.md)|
| schemeTransactionId |    ``` string ```  <br/>  *maxLength: 40  <br/>  example: 019078743804756* <br/> The transaction ID received from schemes for the initial transaction of card on file flows.|
| processor |  [ProcessorData](?path=docs/schemas-md/ProcessorData.md)|
| additionalDetails | [AdditionalTransactionDetails](?path=docs/schemas-md/AdditionalTransactionDetails.md)|
| accountUpdaterResponse |  [AccountUpdaterResponse](?path=docs/schemas-md/AccountUpdaterResponse.md)|
| achResponse |  [AchResponse](?path=docs/schemas-md/AchResponse.md)|
| currencyConversionResponse |  [CurrencyConversionResponse](?path=docs/schemas-md/CurrencyConversionResponse.md)|
| requiredActions | [RequiredActions](?path=docs/schemas-md/RequiredActions.md)|
| plannedDueDate |    ``` string ```  <br/>  *pattern: ^\d{4}-(0[1-9]P1[0-2])-(0[1-9]P[12][0-9]P3[01])$  <br/>  example: 2022-03-03* <br/>  Capture PlannedDueDate field sent for SEPA transactions.|
| networkToken | [NetworkToken](?path=docs/schemas-md/NetworkToken.md)|
| error | [Error](?path=docs/schemas-md/Error.md)|   
  




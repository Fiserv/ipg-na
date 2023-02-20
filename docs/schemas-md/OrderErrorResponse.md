
# OrderErrorResponse

| *description*:   | *Order response with error field included.*|
|----|----|
| clientRequestId |    ``` string ```  <br/>  *example: 30dd879c-ee2f-11db-8314-0800200c9a66*. <br/> Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  <br/>  *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7*. <br/>  Request identifier in API, can be used to request logs from the support team.|
| responseType | ResponseType  <br/>   ``` string ``` <br/>  *example: Unauthenticated*.  <br/> The type of the response. <br/>  Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| orderId |    ``` string ```  <br/>  *example: 123456*. <br/>  Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| billing | [Billing](?path=docs/schemas-md/Billing.md)|  
| shipping | [Shipping](?path=docs/schemas-md/Shipping.md)|  
| mandate | [SepaMandate](?path=docs/schemas-md/SepaMandate.md)|  
| transactions | *example: List [ OrderedMap { "transactionState": "AUTHORIZED", "ipgTransactionId": "838916029301", "transactionType": "SALE", "transactionAmount": OrderedMap { "total": 10.24, "currency": "USD" }, "storeId": "1109959991" } ]* Required for some payment methods (for example, Klarna).|
| additionalDetails | [AdditionalDetails](?path=docs/schemas-md/AdditionalDetails.md)|  
| error | [Error](?path=docs/schemas-md/Error.md)|  
  


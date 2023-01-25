
# OrderErrorResponse

| *description*:   | *Order response with error field included.*|
|----|----|
| clientRequestId |    ``` string ```  *example:   30dd879c-ee2f-11db-8314-0800200c9a66*. Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7*. Request identifier in API, can be used to request logs from the support team.|
| responseType | ResponseType   ``` string ```  *example: Unauthenticated*. The type of the response. Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| orderId |    ``` string ```  *example: 123456*. Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| billing |  |  
| shipping |  |  
| mandate |  |  
| transactions | *example: List [ OrderedMap { "transactionState": "AUTHORIZED", "ipgTransactionId": "838916029301", "transactionType": "SALE", "transactionAmount": OrderedMap { "total": 10.24, "currency": "USD" }, "storeId": "1109959991" } ]* Required for some payment methods (for example, Klarna).|
| additionalDetails |   |  
| error |   |  


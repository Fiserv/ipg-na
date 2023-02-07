
# PaymentUrlErrorResponse

| *description*:   | *Payment URL response with error field included.*|
|----|----|
| clientRequestId |    ``` string ```  *example:   30dd879c-ee2f-11db-8314-0800200c9a66*. Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7*. Request identifier in API, can be used to request logs from the support team.|
| responseType | ResponseType   ``` string ```  *example: Unauthenticated*. The type of the response. Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| requestStatus |    ``` string ```  *example: SUCCESS*. Request status. If it is anything other than 'SUCCESS', please refer to 400s HTTP error codes or decline. See Error object for details. Enum:    > Array [ 4 ] - [ SUCCESS, VALIDATION_FAILED, PROCESSING_FAILED, FAILURE ]|
| orderId |    ``` string ```  *example: 123456*. Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| paymentUrl |    ``` string ```  *example: `https://api.firstdata.com/connect/gateway/processing?storename=123456789&oid=R-96cdbaa4-c22e-4598-a2f1-c2b5fed79ef1&paymentUrlId=d3eb74fe-cf63-47e1-b89f-52ba0cc7965c`*. URL for embedded payment link.|
| expiration |    ``` string ``` ($int64)  *example: 4102358400*. Time until payment URL expires. Returns EPOCH Seconds.|
| transactionId |    ``` string ```  *example: 123978432*. ID code from the transaction.|
| error | [Error](?path=docs/schemas-md/Error.md)|   
  


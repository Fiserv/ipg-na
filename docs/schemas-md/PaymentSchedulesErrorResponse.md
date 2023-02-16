
# PaymentSchedulesErrorResponse

| *description*:   | *Payment schedules response with error field included.*|
|----|----|
| clientRequestId |    ``` string ``` <br/> *example:   30dd879c-ee2f-11db-8314-0800200c9a66*. <br/>  Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  <br/>  *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7*. <br/>  Request identifier in API, can be used to request logs from the support team.|
| responseType | [ResponseType](?path=docs/schemas-md/ResponseType.md)   <br/>  ``` string ```  <br/>  *example: Unauthenticated*. The type of the response. <br/>  Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| requestStatus |    ``` string ```  *example: SUCCESS*. Request status. If it is anything other than 'SUCCESS', please refer to 400s HTTP error codes or decline. See Error object for details. Enum:    > Array [ 4 ] - [ SUCCESS, VALIDATION_FAILED, PROCESSING_FAILED, FAILURE ]|
| orderId |    ``` string ```   <br/> *example: 123456*.  <br/> Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| state | [RecurringPaymentState](?path=docs/schemas-md/RecurringPaymentState.md)  <br/>   ``` string ```  <br/>  *example: Installed*.  <br/> State of the recurring payment.  <br/> Enum:Array [ 3 ] - [ Installed, Inactivated, Cancelled ]|
| transactionResponse | [TransactionResponse](?path=docs/schemas-md/TransactionResponse.md)|
| error | [Error](?path=docs/schemas-md/Error.md)|   
  


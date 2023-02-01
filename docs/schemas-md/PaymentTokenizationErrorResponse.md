
# PaymentTokenizationErrorResponse

| *description*:   | *Payment tokenization response with error field included.*|
|----|----|
| clientRequestId |    ``` string ```  *example:   30dd879c-ee2f-11db-8314-0800200c9a66*. Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7*. Request identifier in API, can be used to request logs from the support team.|
| responseType | ResponseType   ``` string ```  *example: Unauthenticated*. The type of the response. Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| requestStatus |    ``` string ```  *example: DELETED*. Request status. If it is anything other than 'SUCCESS', please refer to 400s HTTP error codes or decline. See Error object for details. Enum:    > Array [ 7 ] - [ DELETED, FAILED, SUCCESS, APPROVED, WAITING, VALIDATION_FAILED, DECLINED ]|
| requestTime |    ``` string ```   *example:   1554308829345*. Time of the request.|
| brand |    ``` integer ``` ($int64) ,  *example:   VISA*. Card brand.|
| country |    ``` integer ``` ($int64) ,  *example:   Germany*. Country of the card issued.|
| paymentToken |    ``` integer ``` ($int64) ,  *example:   Germany*. Country of the card issued.|
| paymentCard |    ``` integer ``` ($int64) ,  *example:   Germany*. Country of the card issued.|
| networkToken |   |  
| processor |   |   
| orderId |    ``` string ```  * maxLength: 14  example: R-44df6542-ae0b-4415-88e8-7f3e62cc9e5d*. Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| ipgTransactionId | ``` string ```  * maxLength: 14  example: 838916029301*. The response transaction ID.|
| merchantTransactionId | ``` string ```  * maxLength: 40  example: lsk23532djljff3*. The unique merchant transaction ID from the request header, if supplied.|
| additionalResponseData |  |
| error | [Error](?path=docs/schemas-md/Error.md)|   
  



# PaymentTokenizationErrorResponse

| *description*:   | *Contains apiTraceId and clientRequestId shared in all response types.*|
|----|----|
| clientRequestId |    ``` string ```   <br/> *example:   30dd879c-ee2f-11db-8314-0800200c9a66*. <br/>  Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  <br/>  *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7*. <br/>  Request identifier in API, can be used to request logs from the support team.|
| responseType | ResponseType   ``` string ```  <br/>  *example: Unauthenticated*.  <br/> The type of the response. <br/>  Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| requestStatus |    ``` string ```  <br/>  *example: DELETED*. <br/>  Request status. If it is anything other than 'SUCCESS', please refer to 400s HTTP error codes or decline. See Error object for details. <br/>  Enum:    > Array [ 7 ] - [ DELETED, FAILED, SUCCESS, APPROVED, WAITING, VALIDATION_FAILED, DECLINED ]|
| requestTime |    ``` string ```   <br/>  *example:   1554308829345*.  <br/> Card brand.|
| brand |    ``` integer ``` <br/>  ($int64)  <br/>  *example:   VISA*.  <br/> Time of the request.|
| country |    ``` integer ```  <br/> ($int64)  <br/>  *example:   Germany*.  <br/> Country of the card issued.|
| paymentToken |    ``` integer ```  <br/> ($int64)  <br/>   *example:   <br/>  Germany*. Country of the card issued.|
| paymentCard |    ``` integer ```  <br/> ($int64)  <br/>   *example:   Germany*.  <br/> Country of the card issued.|
| networkToken | [NetworkToken](?path=docs/schemas-md/NetworkToken.md)|  
| processor | [ProcessorData](?path=docs/schemas-md/ProcessorData.md)|   
| orderId |    ``` string ```   <br/>  maxLength: 14   <br/> *example: R-44df6542-ae0b-4415-88e8-7f3e62cc9e5d*.  <br/> Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| ipgTransactionId | ``` string ```   <br/> maxLength: 14   <br/> *example: 838916029301*.  <br/> The response transaction ID.|
| merchantTransactionId | ``` string ```   <br/>  maxLength: 40   <br/> *example: lsk23532djljff3*.  <br/> The unique merchant transaction ID from the request header, if supplied.|
| additionalResponseData | [AdditionalResponseData](?path=docs/schemas-md/AdditionalResponseData.md)|   
   



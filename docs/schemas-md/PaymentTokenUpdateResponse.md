
# PaymentTokenUpdateResponse

| *description*:   | *Contains apiTraceId and clientRequestId shared in all response types.*|
|----|----|
| clientRequestId |    ``` string ```  *example:   30dd879c-ee2f-11db-8314-0800200c9a66*. Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7*. Request identifier in API, can be used to request logs from the support team.|
| responseType | ResponseType   ``` string ```  *example: Unauthenticated*. The type of the response. Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| requestStatus |    ``` string ```  *example: DELETED*. Request status. If it is anything other than 'SUCCESS', please refer to 400s HTTP error codes or decline. See Error object for details. Enum:    > Array [ 3 ] - [ FAILED, SUCCESS, PARTIAL_SUCCESS ]|
| requestTime |    ``` string ```   *example:   1554308829345*. Card brand.|
| error | [Error](?path=docs/schemas-md/Error.md)|  




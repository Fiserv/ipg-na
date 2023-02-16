
# GetNetworkTokenCryptogramResponse

| *description*:   | *Response for Get Network Token Cryptogram Request*|
|----|----|
| clientRequestId |    ``` string ``` <br/> *example: 30dd879c-ee2f-11db-8314-0800200c9a66* <br/> Echoes back the value in the request header for tracking.| 
| apiTraceId |    ``` string ``` <br/> *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7* <br/> Request identifier in API, can be used to request logs from the support team.|
| responseType | ResponseType   ``` string ``` <br/> *example: Unauthenticated* <br/> The type of the response. <br/> Enum:[ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| requestStatus |    ``` string ``` <br/> *example: SUCCESS* <br/> The status of the request.<br/> Enum:[ FAILED, SUCCESS ]|
| requestTime |    ``` integer ``` <br/> ($int64) <br/> *example: 1554308829345* <br/> Time of the request.|
| networkToken | [NetworkToken](?path=docs/schemas-md/NetworkToken.md)|  







     



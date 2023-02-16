
# ManagedRedirectResponse

| *description*:   | *Response for Managed redirect transaction request*|
|----|----|
| clientRequestId |    ``` string ``` <br/> *example: 30dd879c-ee2f-11db-8314-0800200c9a66* <br/> Echoes back the value in the request header for tracking.|
| apiTraceId |  ``` string ``` <br/> *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7* <br/> Request identifier in API, can be used to request logs from the support team.|  
| responseType | ResponseType  ``` string ``` <br/> *example: Unauthenticated* <br/> The type of the response. <br/> Enum:[ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| requestStatus |  ``` string ``` <br/> *example: SUCCESS* <br/> The status of the request. <br/> Enum:[ SUCCESS, VALIDATION_FAILED, PROCESSING_FAILED, FAILURE ]|
| orderId |  ``` string ``` <br/> *example: 123456* <br/> Note - Client Order ID if supplied by client which should not contain any special characters or spaces. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| redirectURL |  ``` string ``` <br/> *example: https://api.firstdata.com/connect/gateway/processing?storename=123456789&oid=R-96cdbaa4-c22e-4598-a2f1-c2b5fed79ef1&redirectRequestId=d3eb74fe-cf63-47e1-b89f-52ba0cc7965c* <br/>  URL for embedded payment link.|  



     




# PaymentUrlDetailResponse

| *description*:   | *Response from an embedded payment link request.*|
|----|----|
| clientRequestId |    ``` string ```  <br/>  *example: 30dd879c-ee2f-11db-8314-0800200c9a66*  <br/> Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  <br/>  *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7* <br/>  Request identifier in API, can be used to request logs from the support team.|
| responseType | ResponseType   ``` string ```  <br/>  *example: Unauthenticated* <br/> The type of the response. <br/>  Enum: > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| paymentUrlDetails |  Array of payment URL details. [PaymentUrlDetails](?path=docs/schemas-md/BasicResponse.md)|
| industrySpecificExtensions |  [IndustrySpecificExtensions](?path=docs/schemas-md/IndustrySpecificExtensions.md)|    

**PaymentUrlDetailResponse Example:**

```{r}

{
  "clientRequestId": "30dd879c-ee2f-11db-8314-0800200c9a66",
  "apiTraceId": "rrt-0bd552c12342d3448-b-ea-1142-12938318-7",
  "paymentUrl": "https://hyperlink-to-payment.com",
  "orderId": "9723846",
  "requestTime": 1518811817,
  "status": "Created"
}
``` 

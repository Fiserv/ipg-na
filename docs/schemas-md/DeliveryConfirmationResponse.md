
# DeliveryConfirmationResponse

| *description*:   | *Delivery Confirmation response.*|
|----|----|
| clientRequestId |    ``` string ```  *example: 30dd879c-ee2f-11db-8314-0800200c9a66*. Echoes back the value from the request header for tracking.|
| apiTraceId |    ``` string ```   *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7*. Request identifier in API, can be used to request logs from the support team..|
| responseType | ResponseType   ``` string ```   *example: Unauthenticated*. The type of the response. Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| responseCode | ``` string ```  *example: 00*. Response code from endpoints.|
| responseMessage | ``` string ```  *example: Amount specified exceeds allowable limit.*. Message returned from endpoints.|   

**DeliveryConfirmationResponse Example:**

```{r}

{
  "responseCode": "0000",
  "responseMessage": "APPROVED"
}
```

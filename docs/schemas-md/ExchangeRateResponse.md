
# ExchangeRateResponse

| *description*:   | *Exchange rate response.*|
|----|----|
| clientRequestId |    ``` string ```  <br/>  *example:   30dd879c-ee2f-11db-8314-0800200c9a66*. <br/>  Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  <br/>  *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7*.  <br/> Request identifier in API, can be used to request logs from the support team.|
| responseType | [ResponseType](?path=docs/schemas-md/ResponseType.md)  <br/>   ``` string ```  <br/>  *example: Unauthenticated* <br/>  The type of the response.  <br/> Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| ipgTransactionId |    ``` integer ``` ($int64)  *example: 838916029301*. The response transaction ID.|
| requestTime |    ``` string ```   <br/>  *example:   1554308829345*.  <br/> Time of the request. The used format is "yyyy-MM-dd'T'HH:mm:ss.SSSXXX".|
| exchangeRateDetails |   |  

**ExchangeRateResponse Example:**

```{r}

{
  "clientRequestId": "30dd879c-ee2f-11db-8314-0800200c9a66",
  "apiTraceId": "rrt-0bd552c12342d3448-b-ea-1142-12938318-7",
  "requestTime": 1592912760,
  "exchangeRateDetails": {
    "inquiryRateId": 49150,
    "foreignCurrency": "AUD",
    "foreignAmount": "130.33",
    "exchangeRate": "1.2968",
    "dccOffered": "true",
    "exchangeRateSourceTimestamp": "2015-06-23T13:46:00.000+02:00",
    "expirationTimestamp": "2015-06-23T13:46:00.000+02:00",
    "marginRatePercentage": "3",
    "exchangeRateSourceName": "REUTERS WHOLESALE INTERBANK"
  }
}
```

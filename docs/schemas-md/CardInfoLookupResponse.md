
# CardInfoLookupResponse

| *description*:   | *Response from card info lookup request.*|
|----|----|
| clientRequestId |    ``` string ```  *example: 30dd879c-ee2f-11db-8314-0800200c9a66* Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7* Request identifier in API, can be used to request logs from the support team.|
| responseType |    ResponseTypestring  *example: Unauthenticated* The type of the response. Enum:[ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| cardDetails |   [example: List [ OrderedMap { "brand": "VISA", "brandProductId": "VISA BUSINESS", "cardFunction": "CREDIT", "commercialCard": "CORPORATE", "issuerCountry": "DE", "issuerName": "First National Bank of Omaha" } ] One or more card information retrieved based on BIN. [CardInfo](?path=docs/schemas-md/CardInfo.md)]|
| requestStatus |    ``` string ```  *example: SUCCESS* Request status. Enum:[ SUCCESS, LIST_EMPTY ]|


**CardInfoLookupResponse Example:**

```{r}

{
  "cardDetails": [
    {
      "brand": "VISA",
      "brandProductId": "VISA BUSINESS",
      "cardFunction": "CREDIT",
      "commercialCard": "CORPORATE",
      "issuerCountry": "DE",
      "issuerName": "First National Bank of Omaha"
    }
  ],
  "requestStatus": "SUCCESS"
}
```  
  


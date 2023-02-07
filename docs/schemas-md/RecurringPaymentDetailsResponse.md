
# RecurringPaymentDetailsResponse

| *description*:   | *Order response containing recurring payment details.*|
|----|----|
| clientRequestId |    ``` string ```  *example:   30dd879c-ee2f-11db-8314-0800200c9a66*. Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7*. Request identifier in API, can be used to request logs from the support team.|
| responseType | ResponseType   ``` string ```  *example: Unauthenticated*. The type of the response. Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| orderId |    ``` string ```  *example: 123456*. Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| billing | [Billing](?path=docs/schemas-md/Billing.md)|  
| shipping | [Shipping](?path=docs/schemas-md/Shipping.md)|  
| mandate | [SepaMandate](?path=docs/schemas-md/SepaMandate.md)|  
| transactions | *example: List [ OrderedMap { "transactionState": "AUTHORIZED", "ipgTransactionId": "838916029301", "transactionType": "SALE", "transactionAmount": OrderedMap { "total": 10.24, "currency": "USD" }, "storeId": "1109959991" } ]* Required for some payment methods (for example, Klarna).|
| additionalDetails | [AdditionalDetails](?path=docs/schemas-md/AdditionalDetails.md)|
| recurringPaymentDetails | [RecurringPaymentDetails](?path=docs/schemas-md/RecurringPaymentDetails.md)|   
| industrySpecificExtensions |  [IndustrySpecificExtensions](?path=docs/schemas-md/IndustrySpecificExtensions.md)|           

**RecurringPaymentDetailsResponse Example:**

```{r}

{
  "clientRequestId": "30dd879c-ee2f-11db-8314-0800200c9a66",
  "apiTraceId": "rrt-0bd552c12342d3448-b-ea-1142-12938318-7",
  "orderId": "123456",
  "billing": {
    "name": "John Doe",
    "customerId": "1234567890",
    "contact": {
      "email": "John.Doe@example.com",
      "phone": "5555555555"
    }
  },
  "storeId": "1109959991",
  "purchaseOrderNumber": "123055342",
  "invoiceNumber": "96126098",
  "creationDate": "2018-10-25",
  "startDate": "2018-10-25",
  "nextAttemptDate": "2018-10-25",
  "transactionAmount": {
    "total": 10.5,
    "currency": "USD"
  },
  "frequency": {
    "every": 3,
    "unit": "DAY"
  },
  "numberOfPayments": "10",
  "runCount": "3",
  "state": "Installed",
  "comments": "This scheduled payment series is to pay for the thing"
}
```

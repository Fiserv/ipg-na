
# PaymentBrandResponse

| *description*: | *List of available brands of a store.*|
|----|----|
| clientRequestId |    ``` string ```  <br/>   *example: 30dd879c-ee2f-11db-8314-0800200c9a66*  <br/> Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```  <br/>   *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7*  <br/> Request identifier in API, can be used to request logs from the support team.|
| responseType | [ResponseType](?path=docs/schemas-md/ResponseType.md)|  
| brands |    ``` string ```  <br/>   This field contains the brand ID.|  

**PaymentBrandResponse Example:**

```{r}

{
  "clientRequestId": "30dd879c-ee2f-11db-8314-0800200c9a66",
  "apiTraceId": "rrt-0bd552c12342d3448-b-ea-1142-12938318-7",
  "brands": [
    "MASTERCARD",
    "VISA",
    "MAESTRO"
  ]
}
```







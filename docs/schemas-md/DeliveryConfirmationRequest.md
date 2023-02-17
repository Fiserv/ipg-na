
# DeliveryConfirmationRequest

| *description*:   | *Delivery Confirmation generation request.*|
|----|----|
| storeId |    ``` string ```  <br/>  *maxLength: 20  example: 12345500000*.  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| ipgTransactionId |    ``` integer ```  <br/> ($int64)  <br/>  *example: 838916029301*.  <br/> The response transaction ID.|
| merchantTransactionId |    ``` string ```   <br/>  maxLength: 40  <br/> *example: lsk23532djljff3*. <br/>  The unique merchant transaction ID from the request, if supplied.|
| orderId |    ``` string ```  <br/>  *example: 123456*.  <br/> Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| tDate | ``` string ```  <br/>  *example: 1518811817*. <br/>  The transaction time in seconds since epoch.|     

**DeliveryConfirmationRequest Example:**

```{r}

{
  "storeId": "12345500000",
  "ipgTransactionId": 8154886515,
  "merchantTransactionId": "lsk23532djljff3",
  "orderId": "deliveryconfirmation01",
  "tDate": "1518811817"
}
```

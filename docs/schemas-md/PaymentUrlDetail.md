
# PaymentUrlDetail

| *description*:   | *Detailed information about a payment URL.*|
|----|----|
| paymentUrl |    ``` string ```  <br/>  *example: "https://api.firstdata.com/connect/gateway/processing?storename=123456789&oid=R-96cdbaa4-c22e-4598-a2f1-c2b5fed79ef1&paymentUrlId=d3eb74fe-cf63-47e1-b89f-52ba0cc7965c"*  <br/>  URL for embedded payment link.|
| expiration |    ``` number ```  <br/>  *($int64) <br/>  example: 4102358400*  <br/> Expiration time of the payment URL in seconds in the timestamp format.|
| merchantTransactionId |    ``` string ```  <br/>  *maxLength: 40 example: lsk23532djljff3*  <br/> The unique merchant transaction ID from the request, if supplied.|
| orderId |    ``` number ``` <br/>  *example: 123456*  <br/> Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| requestTime |    ``` number ```  <br/> ($int64) <br/>  *example: 1518811817*  <br/> The transaction time in seconds since epoch.|
| status |  [PaymentUrlStatusstring](?path=docs/schemas-md/PaymentUrlStatusstring.md)   ``` number ``` example: Created The status of payment URL. Enum:[ Created, Used, Expired, Cancelled ]*|  











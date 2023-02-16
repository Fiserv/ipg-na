
# AliPay

| *description*:   | *The payment object for AliPay transactions. Use this to populate AliPay payment method details*|
|----|----|
| paymentDataType* |    ``` string ```  <br/> *example: QRCODE* <br/>  Use this to indicate the type of machine-readable payment data for scanning.  <br/> Enum:Array [ 2 ] - [ BARCODE, QRCODE ]|
| paymentData* |    ``` string ```   <br/>  maxLength: 100 <br/>  pattern: ^(?!\s*$).+  <br/> *example: 283047752805604753*  <br/> Use this to send payment-related information, such as customer identity ID.|
| orderTitle* |    ``` string ```    <br/> maxLength: 100 <br/>  pattern: ^(?!\s*$).+  <br/> *example: My Purchase*  <br/> Use this to send an order title that shows up in the statement.|
| orderDetails* |    ``` string ```   <br/> maxLength: 1024 pattern: ^(?!\s*$).+  <br/> *example: These are the details about my purchase.*  <br/> Use this to send order details that show up in the statement.|


**AliPay Example:**

```{r}

{
  "paymentDataType": "BARCODE",
  "paymentData": "283047752805604753",
  "orderTitle": "My Purchase",
  "orderDetails": "These are details about my purchase."
}
```






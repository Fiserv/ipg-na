
# AliPay

| *description*:   | *The payment object for AliPay transactions. Use this to populate AliPay payment method details*|
|----|----|
| paymentDataType* |    ``` string ```   *example: QRCODE* Use this to indicate the type of machine-readable payment data for scanning. Enum:Array [ 2 ] - [ BARCODE, QRCODE ]|
| paymentData* |    ``` string ```   *maxLength: 100 pattern: ^(?!\s*$).+ example: 283047752805604753* Use this to send payment-related information, such as customer identity ID.|
| orderTitle* |    ``` string ```   *maxLength: 100 pattern: ^(?!\s*$).+ example: My Purchase* Use this to send an order title that shows up in the statement.|
| orderDetails* |    ``` string ```   *maxLength: 1024 pattern: ^(?!\s*$).+ example: These are the details about my purchase.* Use this to send order details that show up in the statement.|


**AliPay Example:**

```{r}

{
  "paymentDataType": "BARCODE",
  "paymentData": "283047752805604753",
  "orderTitle": "My Purchase",
  "orderDetails": "These are details about my purchase."
}
```






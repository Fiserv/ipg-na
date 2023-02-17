
# GenerateCashReceiptRequest

| *description*:   | *Generate cash receipt request.*|
|----|----|
| storeId |    ``` string ```  <br/>  maxLength: 20  <br/>  *example: 12345500000*.  <br/> An optional outlet ID for clients that support multiple stores in the same app.|
| ipgTransactionId |    ``` integer ```  <br/> ($int64)  <br/>  *example: 838916029301*.  <br/> The response transaction ID.|
| merchantTransactionId |    ``` string ```  <br/> maxLength: 40  <br/> *example: lsk23532djljff3*.  <br/> The unique merchant transaction ID from the request, if supplied.|
| orderId |    ``` string ```  <br/>  *example: 123456*.  <br/> Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| tDate | ``` string ```  *example: 1518811817*. The transaction time in seconds since epoch.|   
| taxIdentifier | ``` string ```  <br/>  *pattern: [0-9]{1,20} maxLength: 20 example: 01067501461*.|
| receiptType | ``` string ```  <br/>  *example: EXPENSE_STATEMENT_FOR_LICENSEE*.  <br/> Receipt Type is passed from Merchant for Deduction for personal and Expense statement for licensee. <br/>  Enum:Array [ 2 ] - [ DEDUCTION_FOR_PERSONAL, EXPENSE_STATEMENT_FOR_LICENSEE ]|
| billType | ``` string ```  <br/>  *example: TAXABLE*.  <br/> Bill Type is passed from Merchant for tax purpose to KPS. <br/>  Enum:Array [ 2 ] - [ TAXABLE, TAX_FREE ]| 

**GenerateCashReceiptRequest Example:**

```{re}

{
  "storeId": "12345500000",
  "ipgTransactionId": 8154886515,
  "merchantTransactionId": "lsk23532djljff3",
  "orderId": "CashReceipt01",
  "tDate": "1518811817",
  "TaxIdentifier": "01067501461",
  "ReceiptType": "EXPENSE_STATEMENT_FOR_LICENSEE",
  "BillType": "TAXABLE"
}
```


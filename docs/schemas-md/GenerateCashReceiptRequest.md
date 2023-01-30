
# GenerateCashReceiptRequest

| *description*:   | *Generate cash receipt request.*|
|----|----|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| ipgTransactionId |    ``` integer ``` ($int64)  *example: 838916029301*. The response transaction ID.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| orderId |    ``` string ```  *example: 123456*. Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| tDate | ``` string ```  *example: 1518811817*. The transaction time in seconds since epoch.|   
| taxIdentifier | ``` string ```  *pattern: [0-9]{1,20} maxLength: 20 example: 01067501461*.|
| receiptType | ``` string ```  *example: EXPENSE_STATEMENT_FOR_LICENSEE*. Receipt Type is passed from Merchant for Deduction for personal and Expense statement for licensee. Enum:Array [ 2 ] - [ DEDUCTION_FOR_PERSONAL, EXPENSE_STATEMENT_FOR_LICENSEE ]|
| billType | ``` string ```  *example: TAXABLE*. Bill Type is passed from Merchant for tax purpose to KPS. Enum:Array [ 2 ] - [ TAXABLE, TAX_FREE ]| 


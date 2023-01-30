
# PaymentMethodPaymentSchedulesRequest

| *description*:   | *Request to create a new payment schedule using a payment method.*|
|----|----|
| requestType |    ``` string ```  *example:   PaymentMethodPaymentSchedulesRequest*. Object name of the payment schedules request.|
| storeId |    ``` string ```  *maxLength: 20  example: 1109959991*. Store ID number.|
| startDate |   ``` string ``` ($date)   *example: 2018-10-25*. Date of mandate signature.|
| numberOfPayments |    ``` integer ``` ($int32)  *minimum: 1 maximum: 999  example: 10  example: 10*.  Number of times the recurring payment will process.|
| maximumFailures |    ``` integer ``` ($int32)  *minimum: 1 maximum: 999  example: 10  example: 1*.  Number of failures that can be encountered before re-tries cease.|
| invoiceNumber |   ``` string ```  *example: 96126098*. Invoice number.|
| purchaseOrderNumber |   ``` string ```  *example: 123055342*. Purchase order number.|
| transactionOrigin |  TransactionOrigin  ``` string ```  *example: ECOM*.The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| dynamicMerchantName |   ``` string ```  *example: MyWebsite*. Dynamic merchant name for the cardholder's statement.|
| frequency |   |
| transactionAmount |   |
| clientLocale |   |
| orderId |    ``` string ```  *example: 123456*. Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| billing |   |
| shipping |   |
| industrySpecificExtensions |   |
| comments |    ``` string ```  *example: This scheduled payment series is to pay for the thing.*. User supplied comments.|
| paymentMethod |   |
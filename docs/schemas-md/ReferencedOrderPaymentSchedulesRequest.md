
# ReferencedOrderPaymentSchedulesRequest

| *description*:   | *Request to create a new payment schedule using a payment method.*|
|----|----|
| requestType |    ``` string ```  *example:  PaymentMethodPaymentSchedulesRequest*. Object name of the payment schedules request.|
| storeId |    ``` string ```  *maxLength: 20  example: 1109959991*. Store ID number.|
| startDate |   ``` string ``` ($date)   *example: 2018-10-25*. Date of mandate signature.|
| numberOfPayments |    ``` integer ``` ($int32)  *minimum: 1 maximum: 999  example: 10  example: 10*.  Number of times the recurring payment will process.|
| maximumFailures |    ``` integer ``` ($int32)  *minimum: 1 maximum: 999  example: 10  example: 1*.  Number of failures that can be encountered before re-tries cease.|
| invoiceNumber |    ``` string ```  *example: 96126098*. Invoice number.|
| purchaseOrderNumber |    ``` string ```  *example: 123055342*. Purchase order number.|
| transactionOrigin |  transactionOrigin  ``` string ```  *example: ECOM*. The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| dynamicMerchantName |   ``` string ```  *example: MyWebsite*.Dynamic merchant name for the cardholder's statement.|
| frequency | [Frequency](?path=docs/schemas-md/Frequency.md)|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| clientLocale | [ClientLocale](?path=docs/schemas-md/ClientLocale.md)|
| orderId |    ``` string ```  *example: 123456*. Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| billing | [Billing](?path=docs/schemas-md/Billing.md)|  
| shipping | [Shipping](?path=docs/schemas-md/Shipping.md)|
| industrySpecificExtensions |  [IndustrySpecificExtensions](?path=docs/schemas-md/IndustrySpecificExtensions.md)|
| comments |    ``` string ```  *example: This scheduled payment series is to pay for the thing.*. User supplied comments.|
| referencedOrderId |  ``` string ```  *pattern: ^(?!\s*$).+  example: R-f9c2c198-b7cc-491a-a711-93d22fd0e589* Order ID used to create recurring payment from existing transaction.|  

**ReferencedOrderPaymentSchedulesRequest Example:**

```{r}

{
  "requestType": "ReferencedOrderPaymentSchedulesRequest",
  "referencedOrderId": "R-f9c2c198-b7cc-491a-a711-93d22fd0e589",
  "startDate": "2021-12-31",
  "numberOfPayments": 10,
  "maximumFailures": 1,
  "invoiceNumber": "96126098",
  "purchaseOrderNumber": "123055342",
  "transactionOrigin": "ECOM",
  "dynamicMerchantName": "MyWebsite",
  "frequency": {
    "every": 1,
    "unit": "MONTH"
  },
  "transactionAmount": {
    "total": 25.24,
    "currency": "GBP"
  },
  "clientLocale": {
    "language": "EN",
    "country": "USA"
  }
}
```

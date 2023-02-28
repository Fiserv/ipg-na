
# PaymentMethodPaymentSchedulesRequest

| *description*:   | *Request to create a new payment schedule using a payment method.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example:   PaymentMethodPaymentSchedulesRequest* <br/> Object name of the payment schedules request.|
| storeId |    ``` string ```  <br/> maxLength: 20   <br/> example: 1109959991* <br/> Store ID number.|
| startDate |   ``` string ```  <br/> ($date)   <br/>  *example: 2018-10-25* <br/> Date of mandate signature.|
| numberOfPayments |    ``` integer ``` <br/>  ($int32)  <br/> minimum: 1 <br/> maximum: 999 <br/> *example: 10*  <br/> Number of times the recurring payment will process.|
| maximumFailures |    ``` integer ```  <br/> ($int32)  <br/> minimum: 1  <br/> maximum: 999   <br/> *example: 10  example: 1* <br/> Number of failures that can be encountered before re-tries cease.|
| invoiceNumber |   ``` string ```  <br/> *example: 96126098* <br/> Invoice number.|
| purchaseOrderNumber |   ``` string ```  <br/>  *example: 123055342* <br/> Purchase order number.|
| transactionOrigin |  [TransactionOrigin](?path=docs/schemas-md/TransactionOrigin.md)  <br/>  ``` string ```  <br/>  *example: ECOM*  <br/> The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| dynamicMerchantName |   ``` string ```  <br/>  *example: MyWebsite* <br/>  Dynamic merchant name for the cardholder's statement.|
| frequency | [Frequency](?path=docs/schemas-md/Frequency.md)|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| clientLocale | [ClientLocale](?path=docs/schemas-md/ClientLocale.md)|
| orderId |    ``` string ```  *example: 123456*. Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| billing | [Billing](?path=docs/schemas-md/Billing.md)|  
| shipping | [Shipping](?path=docs/schemas-md/Shipping.md)|  | industrySpecificExtensions |  [IndustrySpecificExtensions](?path=docs/schemas-md/IndustrySpecificExtensions.md)|
| comments |    ``` string ```  *example: This scheduled payment series is to pay for the thing.*. User supplied comments.|
| paymentMethod | [PaymentCardPaymentMethod](?path=docs/schemas-md/PaymentCardPaymentMethod.md)|       

**PaymentMethodPaymentSchedulesRequest Example:**

```{r}

{
  "requestType": "PaymentMethodPaymentSchedulesRequest",
  "transactionAmount": {
    "total": 25.24,
    "currency": "GBP"
  },
  "startDate": "2021-12-31",
  "frequency": {
    "every": 1,
    "unit": "MONTH"
  },
  "paymentMethod": {
    "paymentCard": {
      "number": "5424180279791732",
      "expiryDate": {
        "month": "12",
        "year": "25"
      },
      "securityCode": "977",
      "brand": "VISA"
    }
  }
}
```

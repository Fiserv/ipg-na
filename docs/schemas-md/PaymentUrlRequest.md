
# PaymentUrlRequest

| *description*:   | *Request to generate an embedded payment link.*|
|----|----|
storeId |    ``` string ```   *maxLength: 20 example: 12345500000* An optional Outlet ID for clients that support multiple stores in the same developer app.|
| clientLocale | [ClientLocale](?path=docs/schemas-md/ClientLocale.md)| 
| transactionAmount* | [Amount](?path=docs/schemas-md/Amount.md)| 
| transactionType | TransactionTypestring   ``` string ```   *example: SALE* Type of transaction to perform. Primary transaction types in requests include 'SALE', 'PREAUTH', 'CREDIT' and 'FORCED_TICKET'. Enum:[ SALE, PREAUTH, CREDIT, FORCED_TICKET, VOID, RETURN, POSTAUTH, PAYER_AUTH, DISBURSEMENT ]|
| orderId |    ``` string ```   *example: 123456* Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| billing | [Billing](?path=docs/schemas-md/Billing.md)|
| shipping | [Shipping](?path=docs/schemas-md/Shipping.md)|
| industrySpecificExtensions |  [IndustrySpecificExtensions](?path=docs/schemas-md/IndustrySpecificExtensions.md)|
| transactionNotificationURL |    ``` string ```   *example: "https://showmethepaymentresult.com" * URL for notifying merchant of payment result.|
| expiration |    ``` integer ```   *($int64) example: 4102358400* Expiration time of the payment URL in seconds in the timestamp format.|
| authenticateTransaction |    ``` boolean ```   *example: true* If 3D secure should be applied.|
| dynamicMerchantName |    ``` boolean ```   *example: MyWebsite* Dynamic merchant name for the cardholder's statement.|
| invoiceNumber |    ``` boolean ```   *example: 96126098* Invoice number.|
| purchaseOrderNumber |    ``` boolean ```   *example: 123055342* Purchase order number.|
| hostedPaymentPageText |    ``` string ```   *maxLength: 255 example: This is a payment for x* The text to be displayed to the payer on the hosted payment page.|
| ip |    ``` string ```   *example: 264.31.73.24* IPv4 or IPv6 network address.|
| revolvingOptions | [RevolvingOptions](?path=docs/schemas-md/RevolvingOptions.md)| 
| installmentOptions | [InstallmentOptions](?path=docs/schemas-md/InstallmentOptions.md)| 
| basket | [Basket](?path=docs/schemas-md/Basket.md)| 


**PaymentUrlRequest Example:**

```{r}

{
  "transactionAmount": {
    "total": 42.42,
    "currency": "USD"
  },
  "transactionType": "SALE",
  "transactionNotificationURL": "https://showmethepaymentresult.com",
  "expiration": 4102358400,
  "authenticateTransaction": true,
  "dynamicMerchantName": "MyWebsite",
  "invoiceNumber": "96126098",
  "purchaseOrderNumber": "123055342",
  "ip": "264.31.73.24",
  "revolvingOptions": {
    "revolvingPayment": true
  },
  "installmentOptions": {
    "numberOfInstallments": 6,
    "installmentsInterest": false
  }
}
```






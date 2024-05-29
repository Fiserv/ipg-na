
# Order

| *description*:   | *Use this model to provide order related details.*|
|----|----|
| orderId |    ``` string ```   <br/>  *maxLength: 100  <br/> example: ABC12345*  <br/> Note - Client Order ID if supplied by client. If not supplied by client, IPG will generate. The first 12 alphanumeric digits are passed down to Fiserv Enterprise reporting tool, Clientline and Data File Manager (DFM).|
| purposeOfPaymentCode |    ``` string ```   <br/>  *maxLength: 12  <br/> example: ABC12345*  <br/> Merchants accepting cards issued in India, Bangladesh, Argentina and/or Egypt require it for VISA Original Credit Transfer Transactions.|
| billing | [Billing](?path=docs/schemas-md/Billing.md)|  
| shipping | [Shipping](?path=docs/schemas-md/Shipping.md)|
| industrySpecificExtensions | [IndustrySpecificExtensions](?path=docs/schemas-md/IndustrySpecificExtensions.md)|
| purchaseCard | [PurchaseCards](?path=docs/schemas-md/PurchaseCards.md)|
| ip | 	IPAddress   ``` string ```  <br/>   *example: 264.31.73.24* <br/>  IPv4 or IPv6 network address.|
| installmentOptions | [InstallmentOptions](?path=docs/schemas-md/InstallmentOptions.md)|
| revolvingOptions | [RevolvingOptions](?path=docs/schemas-md/RevolvingOptions.md)|
| standInDetails | [StandInDetails](?path=docs/schemas-md/StandInDetails.md)|
| tokenCryptogram | [TokenCryptogram](?path=docs/schemas-md/TokenCryptogram.md)   <br/>  ``` string ```  <br/>   *minLength: 20  <br/> maxLength: 32  <br/> example: gfgF92JHDJFjxcJHCQ23IbI12D* <br/>  Network token cryptogram value.|
| softDescriptor | [SoftDescriptor](?path=docs/schemas-md/SoftDescriptor.md)|
| additionalDetails | [AdditionalDetails](?path=docs/schemas-md/AdditionalDetails.md)|
| bancontactQR | [BancontactQR](?path=docs/schemas-md/BancontactQR.md)|
| clientLocale | [ClientLocale](?path=docs/schemas-md/ClientLocale.md)|
| basket | [Basket](?path=docs/schemas-md/Basket.md)| 


**Order Example:**

```{r}

{
  "orderId": "ABC12345",
  "purposeOfPaymentCode": "ISCCRD",
  "additionalDetails": {
    "comments": "This is Token Disbursement transaction",
    "invoiceNumber": "984424645416",
    "purchaseOrderNumber": "4545623458",
    "businessApplicationIdentifier": "ACCOUNT_TO_ACCOUNT",
    "transactionTypeIdentifier": "BUSINESS_DISBURSEMENT_MONEY_SEND"
  },
  "billing": {
    "name": "John Doe",
    "customerId": "1234567890"
  },
  "shipping": {
    "name": "John Doe",
    "address": {
      "address1": "123 Main St.",
      "city": "Sandy Springs",
      "region": "Georgia",
      "postalCode": "30303",
      "country": "USA"
    }
  }
}
```






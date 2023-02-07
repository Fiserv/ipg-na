
# PaymentDevicePaymentMethod

| *description*:   | *Payment method containing payment device information.*|
|----|----|
| paymentDevice* |  [PaymentDevice](?path=docs/schemas-md/PaymentDevice.md)|
| paymentFacilitator* |  [PaymentFacilitator](?path=docs/schemas-md/PaymentFacilitator.md)|


**PaymentDevicePaymentMethod Example:**

```{r}

{
  "paymentDevice": {
    "deviceType": "SWIPE",
    "data": "02A600C0170018008292;5424********1732=1810?*B73CD8C26233D4FFEC5500ED394439D97DDA5F530942D21D0000000000000000000000000000000000000000363434543035353734326299492410027300000260DC03",
    "securityCode": "977",
    "cardholderName": "First Cardholder",
    "cardFunction": "CREDIT",
    "brand": "VISA"
  },
  "paymentFacilitator": {
    "externalMerchantId": "12345",
    "paymentFacilitatorId": "123123123",
    "saleOrganizationId": "123124214",
    "name": "First Reseller",
    "subMerchantData": {
      "mcc": "1432",
      "legalName": "First Merchant",
      "timezone": "Europe/London",
      "address": {
        "address1": "123 Main St.",
        "city": "Sandy Springs",
        "region": "Georgia",
        "postalCode": "30303",
        "country": "USA"
      },
      "document": {
        "type": "NATIONAL_IDENTITY",
        "number": "12345666544"
      },
      "merchantId": "12435325235"
    }
  }
}
``` 






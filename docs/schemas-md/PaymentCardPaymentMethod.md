
# PaymentCardPaymentMethod

| *description*:   | *Payment method containing payment card information.*|
|----|----|
| paymentCard* |  [PaymentCard](?path=docs/schemas-md/PaymentCard.md)|
| paymentFacilitator* |  [PaymentFacilitator](?path=docs/schemas-md/PaymentFacilitator.md)|


**PaymentCardPaymentMethod Example:**

```{r}

{
  "paymentCard": {
    "number": "5424180279791732",
    "expiryDate": {
      "month": "12",
      "year": "25"
    },
    "securityCode": "977"
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






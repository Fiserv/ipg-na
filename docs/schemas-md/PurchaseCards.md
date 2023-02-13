
# PurchaseCards

| *description*:   | *Purchase card details.*|
|----|----|
| Level2 | [Level2](?path=docs/schemas-md/Level2.md)| 
| Level3 | {[lineItems](?path=docs/schemas-md/LineItems.md)}| 


**PurchaseCards Example:**

```{r}

{
  "Level2": {
    "customerReferenceID": "abcdef123xyz",
    "supplierInvoiceNumber": "0000000065348",
    "supplierVATRegistrationNumber": "10001174242",
    "totalDiscountAmountAndRate": {
      "amount": 5.145,
      "rate": 1.175
    },
    "vatShippingAmountAndRate": {
      "amount": 6.03,
      "rate": 1.175
    },
    "dutyAmountAndRate": {
      "amount": 7.03,
      "rate": 1.175
    }
  },
  "Level3": {
    "lineItems": [
      {
        "commodityCode": "ab12",
        "productCode": "0001212120888",
        "description": "Dinner and movie",
        "quantity": 5,
        "unitMeasure": "25",
        "unitPrice": 30.075,
        "vatAmountAndRate": {
          "amount": 5.145,
          "rate": 1.175
        },
        "discountAmountAndRate": {
          "amount": 6.03,
          "rate": 1.175
        },
        "lineItemTotal": 39.075
      }
    ]
  }
}
```






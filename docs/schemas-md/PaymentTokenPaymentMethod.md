
# PaymentTokenPaymentMethod

| *description*:   | *Payment method containing payment tokenization information.*|
|----|----|
| paymentToken* |  [UsePaymentToken](?path=docs/schemas-md/UsePaymentToken.md)|
| paymentFacilitator* |  [PaymentFacilitator](?path=docs/schemas-md/PaymentFacilitator.md)|


**PaymentTokenPaymentMethod Example:**

```{r}

{
  "paymentToken": {
    "value": "1235325235236",
    "function": "DEBIT",
    "securityCode": "977"
  }
}
```





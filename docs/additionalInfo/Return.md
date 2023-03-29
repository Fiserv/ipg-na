
# Return (aka Refund)


## Step 5: Giving Money Back When Goods Have Been Returned

If you want to return funds to a customer's card against an existing order, you can use the Order ID as a reference so that you do not need to submit card details for this activity. You can return the full amount of the order or a partial amount.

### Initiate a Return Using REST API

There are two options to initiate a Return using the API:

|   |   |
|---|---|
|__POST:__ /orders/{order_id}| Use /orders and the Order ID to reference to the order where you want to perform a full or partial refund and include the amount and currency to be returned in the payload|
| __POST:__ /payments/{transaction_id} |Use /payments and the Transaction ID (ipgTransactionId or merchantTransactionId) if you want to send a full or partial refund for a specific transaction and include the amount and currency to be returned in the payload|


### REST API Request Example

```

{
  "requestType": "ReturnTransaction",
  "transactionAmount": {
    "total": "20.00",
    "currency": "USD"
  }
}

```

> [REST API Reference](?path=docs/schemas-md/ReturnTransaction.md)
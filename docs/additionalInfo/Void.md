
# Void


## Step 4: Voiding a Transaction

If your customer has canceled the order or you detect suspicious order details, you can void the transaction referencing the original Transaction ID.

|   |   |
|---|---|
| __POST:__ /payments/{transaction_id} | Use /payments and the Transaction ID (ipgTransactionId or merchantTransactionId) to reference to the specific transaction that you want to void.|

### REST API Request Example

```

{
  "requestType": "VoidTransaction"
}

```

> [REST API Reference](?path=docs/schemas-md/VoidTransaction.md)
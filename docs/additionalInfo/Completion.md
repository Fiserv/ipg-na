
# Completion (Post-Authorization)

## Step 3: Completion When Goods Get Shipped

If you have used the transaction type Pre-Authorization when your customer checked out in your webshop, funds have been reserved on the customer's card account but have not been transferred to your account yet.

In order to complete a transaction and initiate the settlement process, you will need to send a Post-Authorization (postauth) via our API or initiate the completion manually using our Virtual Terminal.

|   |   |
|---|---|
|__POST:__ /orders/{order_id}| Use /orders and the Order ID to reference to the order with the pre-authorized balance |
| __POST:__ /payments/{transaction_id} | 	Use /payments and the Transaction ID <br/> (ipgTransactionId or merchantTransactionId) if you want to reference to a specific pre-authorization transaction that you want to complete |

### REST API Request Example

```
	
{
  "requestType": "PostAuthTransaction",
  "transactionAmount": {
    "total": "28.59",
    "currency": "GBP"
  }
}

```

> [REST API Reference](?path=docs/schemas-md/PaymentCardPreAuthTransaction.md)
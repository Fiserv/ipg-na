
# Recurring payments with stored credentials


# Recurring payments with stored credentials

If you have set up an agreement with your customer to initiate recurring transactions on their behalf (e.g. for subscription payments) and have created a token for their card details, the API request type **PaymentTokenSaleTransaction** allows you to process the regular charges.

Include the following parameters in order to reference back to the original authorization and cardholder authentication where applicable:

|paymentToken||
|---|---|
|value|Include the token that you have defined or obtained when tokenizing the customer's card details|

|storedCredentials||
|---|---|
|sequence|Set this to "SUBSEQUENT" in order to indicate that this is not the first transaction with this customer but part of a series of transactions that you submit on their behalf after the customer has set up the agreement with you.|
|scheduled|Set this to 'true' in order to indicate that this is a recurring transaction (regular interval).|
|referencedSchemeTransactionId|If you received a Scheme Transaction ID in the response to your original authorization (e.g. a zero-value authorization when storing the card details), include this reference in order to link back the transaction to the original agreement.|
|initiator|Set this to "MERCHANT" in order to indicate that you initiated this transaction with no direct involvement of the customer.|

## REST API Request Example

```

{
  "transactionAmount": {
    "total": "12.04",
    "currency": "EUR"
  },
  "requestType": "PaymentTokenSaleTransaction",
  "paymentMethod": {
    "paymentToken": {
      "value": "12345",
    }
  },
  "storedCredentials": {
    "sequence": "SUBSEQUENT",
    "scheduled": true
    "referencedSchemeTransactionId": "098765432112345"
    "initiator": "MERCHANT",
  }
}

```

> [REST API Reference](?path=docs/schemas-md/PaymentTokenSaleTransaction.md)

> [Recurring Payments main page](?path=docs/additionalInfo/RecurringPayments.md)
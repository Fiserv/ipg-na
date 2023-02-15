
# FraudRegistrationError

| *description*: | *Error occurred during the registration.*|
|----|----|
| messages | [ErrorMessage](?path=docs/schemas-md/ErrorMessage.md)|

**FraudRegistrationError Example:**

```{r}

{
  "messages": [
    {
      "code": "invalid_transaction_type",
      "description": "The transaction type is not supported"
    },
    {
      "code": "missing_originalTransactionType",
      "description": "Original Transaction Type is missing or invalid"
    }
  ]
}
```  






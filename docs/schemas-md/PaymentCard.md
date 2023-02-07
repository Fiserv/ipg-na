
# PaymentCard

| *description*: | *Payment card model.*|
|----|----|
| number* |  ``` string ```  *pattern: [0-9]{13,19} example: 5424180279791732.* Payment card number. Can also be an IBAN for Sepa Direct Debit transactions.|
| expiryDate | [Expiration](?path=docs/schemas-md/Expiration.md)|
| securityCode |  ``` string ```  *minLength: 3 maxLength: 4 example: 977.* Card verification value/number.|
| bic |  ``` string ```  *pattern: [A-Z]{4}[A-Z]{2}[A-Z0-9]{2}(XXX|[A-WY-Z0-9][A-Z0-9]{2})? example: PBNKDEFFXXX.* Bank identifier code (BIC) for Sepa Direct Debit.|
| bankCode |  ``` string ```  *pattern: ([0-9]{8})|([A-Z]{4}DE([A-Z0-9][A-NP-Z0-9])(XXX|[A-WY-Z0-9][A-Z0-9]{2})?) example: 10010010.* Bank code for Sepa Direct Debit.|
| cardFunction |  CardFunction ``` string ```  * example: DEBIT Card function.* This field is required when performing transactions for Brazil merchants. Enum:[ CREDIT, DEBIT, PREPAID, VOUCHER, UNDEFINED ]|
| cardholderName |  ``` string ```  *maxLength: 96 example: John Doe.* Name of the cardholder. Note - Only supported with request payload.|
| bin |  ``` string ```  *example: 403587.* The payment card BIN.|
| last4 |  ``` string ```  *example: 4977.* The last 4 numbers of a payment card.|
| brand |  ``` string ```  *example: VISA.* Required only if using dual branded card.|



**PaymentCard Example:**

```{r}

{
  "number": "5424180279791732",
  "expiryDate": {
    "month": "12",
    "year": "25"
  },
  "securityCode": "977"
}
```  



# PaymentCard

| *description*: | *Payment card model.*|
|----|----|
| number* |  ``` string ```  <br/> pattern: [0-9]{13,19} <br/> * example: 5424180279791732.*  <br/> Payment card number. Can also be an IBAN for Sepa Direct Debit transactions.|
| expiryDate | [Expiration](?path=docs/schemas-md/Expiration.md)|
| securityCode |  ``` string ```   <br/> minLength: 3  <br/> maxLength: 4  <br/> *example: 977.*  <br/> Card verification value/number.|
| bic |  ``` string ```  <br/> pattern: [A-Z]{4}[A-Z]{2}[A-Z0-9]{2}(XXX|[A-WY-Z0-9][A-Z0-9]{2})?  <br/> *example: PBNKDEFFXXX*  <br/> Bank identifier code (BIC) for Sepa Direct Debit.|
| bankCode |  ``` string ```   <br/> pattern: ([0-9]{8})|([A-Z]{4}DE([A-Z0-9][A-NP-Z0-9])(XXX|[A-WY-Z0-9][A-Z0-9]{2})?)  <br/> *example: 10010010*  <br/> Bank code for Sepa Direct Debit.|
| cardFunction |  [CardFunction](?path=docs/schemas-md/CardFunction.md)  <br/>  ``` string ```   <br/> * example: DEBIT Card function.*  <br/> This field is required when performing transactions for Brazil merchants.  <br/> Enum:[ CREDIT, DEBIT, PREPAID, VOUCHER, UNDEFINED ]|
| cardholderName |  ``` string ```   <br/> maxLength: 96  <br/> *example: John Doe*  <br/> Name of the cardholder. Note - Only supported with request payload.|
| bin |  ``` string ```   <br/> *example: 403587*  <br/> The payment card BIN.|
| last4 |  ``` string ```   <br/> *example: 4977*  <br/> The last 4 numbers of a payment card.|
| brand |  ``` string ```   <br/> *example: VISA*  <br/> Required only if using dual branded card.|



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


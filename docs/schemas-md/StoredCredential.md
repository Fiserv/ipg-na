
# StoredCredential

| *description*:   | *Object for sending stored credentials.*|
|----|----|
| sequence* |   ``` string ```   *example: FIRST* Indicates if the transaction is first or subsequent. Valid values are First and 'SUBSEQUENT'. Enum:[ FIRST, SUBSEQUENT ]|
| scheduled* |   ``` boolean ```   *example: true* Indicates if the transaction is scheduled or part of an installment.|
| referencedSchemeTransactionId |  ``` string ```   *maxLength: 50 example: 019087868716215* The transaction ID received from schemes for the initial transaction. May be required if sequence is 'SUBSEQUENT'.|
| initiator |  ``` string ```   *example: MERCHANT* Indicates whether it is a merchant-initiated or explicitly consented to by card holder. Valid values are 'MERCHANT' and 'CARDHOLDER'. Enum:[ MERCHANT, CARDHOLDER ]|
| indicatorSubcategory | 	 ``` string ```   *example: CREDENTIAL_ON_FILE_FIRST* For initiator as CARDHOLDER- CREDENTIAL_ON_FILE_FIRST, CREDENTIAL_ON_FILE_SUBSEQUENT, STANDING_ORDER, SUBSCRIPTION, INSTALLMENT are the valid values of indicatorSubcatogory. |For initiator as MERCHANT- UNSCHEDULED_CREDENTIAL_ON_FILE, STANDING_ORDER, SUBSCRIPTION, INSTALLMENT, PARTIAL_SHIPMENT, DELAYED_CHARGE, NO_SHOW_CHARGE, RESUBMISSION are the valid values as indicatorSubcategory. |Not valid values will be ignored. Enum:[ CREDENTIAL_ON_FILE_FIRST, CREDENTIAL_ON_FILE_SUBSEQUENT, UNSCHEDULED_CREDENTIAL_ON_FILE, STANDING_ORDER, SUBSCRIPTION, INSTALLMENT, PARTIAL_SHIPMENT, DELAYED_CHARGE, NO_SHOW_CHARGE, RESUBMISSION ]|


**StoredCredential Example:**

```{r}

{
  "sequence": "SUBSEQUENT",
  "scheduled": false,
  "referencedSchemeTransactionId": "019087868716215",
  "initiator": "CARDHOLDER"
}
```






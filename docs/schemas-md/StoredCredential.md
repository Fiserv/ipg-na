
# StoredCredential

| *description*:   | *Object for sending stored credentials.*|
|----|----|
| sequence* |   ``` string ```    <br/> *example: FIRST* <br/>  Indicates if the transaction is first or subsequent. Valid values are First and 'SUBSEQUENT'. <br/>  Enum:[ FIRST, SUBSEQUENT ]|
| scheduled* |   ``` boolean ```   <br/>  *example: true*  <br/> Indicates if the transaction is scheduled or part of an installment.|
| referencedSchemeTransactionId |  ``` string ```  <br/>   maxLength: 50  <br/> *example: 019087868716215*  <br/> The transaction ID received from schemes for the initial transaction. May be required if sequence is 'SUBSEQUENT'.|
| initiator |  ``` string ```   <br/>  *example: MERCHANT* <br/>  Indicates whether it is a merchant-initiated or explicitly consented to by card holder. Valid values are 'MERCHANT' and 'CARDHOLDER'.  <br/> Enum:[ MERCHANT, CARDHOLDER ]|
| indicatorSubcategory | 	 ``` string ```   <br/>  *example: CREDENTIAL_ON_FILE_FIRST* <br/>  For initiator as  <br/> CARDHOLDER- CREDENTIAL_ON_FILE_FIRST,  <br/> CREDENTIAL_ON_FILE_SUBSEQUENT,  <br/> STANDING_ORDER, SUBSCRIPTION,  <br/> INSTALLMENT <br/> are the valid values of indicatorSubcatogory.  <br/> For initiator as MERCHANT-  <br/> UNSCHEDULED_CREDENTIAL_ON_FILE,  <br/> STANDING_ORDER,  <br/> SUBSCRIPTION,  <br/> INSTALLMENT,  <br/> PARTIAL_SHIPMENT,  <br/> DELAYED_CHARGE,  <br/> NO_SHOW_CHARGE, RESUBMISSION  <br/> are the valid values as indicatorSubcategory.  <br/> Not valid values will be ignored.  <br/> Enum:[ CREDENTIAL_ON_FILE_FIRST, CREDENTIAL_ON_FILE_SUBSEQUENT, UNSCHEDULED_CREDENTIAL_ON_FILE, STANDING_ORDER, SUBSCRIPTION, INSTALLMENT, PARTIAL_SHIPMENT, DELAYED_CHARGE, NO_SHOW_CHARGE, RESUBMISSION ]|


**StoredCredential Example:**

```{r}

{
  "sequence": "SUBSEQUENT",
  "scheduled": false,
  "referencedSchemeTransactionId": "019087868716215",
  "initiator": "CARDHOLDER"
}
```






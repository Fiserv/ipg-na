
# RecurringPaymentDetailsResponse

| *description*:   | *Details about existing gateway schedule.*|
|----|----|
| storeId |    ``` string ```  <br/>  *example: 30dd879c-ee2f-11db-8314-0800200c9a66* <br/>  Store ID number.|
| purchaseOrderNumber |    ``` string ```  <br/>  *example: 123055342* <br/>  Purchase order number.|
| invoiceNumber |    ``` string ```  <br/> *example: 96126098* <br/> Invoice number.| 
| additionalDetails | [AdditionalDetails](?path=docs/schemas-md/AdditionalDetails.md)|  
| creationDate |    ``` string ```  <br/>  *example: Tue Jul 14 13:40:26 IST 2020*   <br/> Deprecated. Please use creationDateFormatted. This may be removed in a future release. Date recurring payment was created.|
| startDate |    ``` string ```  <br/>  *example: Tue Jul 14 13:40:26 IST 2020* <br/>   Deprecated. Please use startDateFormatted. This may be removed in a future release. Date of mandate signature.|
| nextAttemptDate |    ``` string ```  <br/> *example:  Tue Jul 14 13:40:26 IST 2020*.  <br/> Deprecated. Please use nextAttemptDateFormatted. This may be removed in a future release. Date of next transaction process attempt.|
| creationDateFormatted |    ``` string ```  <br/>  *example: 2018-10-25* <br/> Date recurring payment was created.|
| startDateFormatted |    ``` string ```  <br/>  *example: 2018-10-25* <br/>  Date of mandate signature.|
| nextAttemptDateFormatted |    ``` string ```  *example: 2018-10-25*. Date of next transaction process attempt.
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| paymentMethodDetails | [PaymentMethodDetails](?path=docs/schemas-md/PaymentMethodDetails.md)|
| frequency | [Frequency](?path=docs/schemas-md/Frequency.md)|
| numberOfPayments |    ``` integer ``` <br/>  ($int32)  <br/>  *minimum: 1  <br/> maximum: 999  <br/> example: 10* <br/> Number of times the recurring payment will process.|
| runCount |    ``` integer ``` ($int32)  <br/>  *minimum: 0 <br/>  maximum: 999  <br/> example: 10* <br/>  Times the recurring payment has already run.|
| state | RecurringPaymentState   ``` string ``` <br/>   *example: Installed* <br/>  Installed.  <br/> Enum:Array [ 3 ] - [ Installed, Inactivated, Cancelled ]|
| comments |    ``` string ```  <br/>  *example: This scheduled payment series is to pay for the thing* <br/>  User supplied comments.|  

**RecurringPaymentDetails Example:**

```{r}

{
  "storeId": "1109959991",
  "invoiceNumber": "96126098",
  "creationDate": "2018-10-25",
  "startDate": "2018-10-25",
  "transactionAmount": {
    "total": 10.24,
    "currency": "USD"
  },
  "frequency": {
    "every": 3,
    "unit": "DAY"
  },
  "numberOfPayments": 10,
  "runCount": 3,
  "state": "Installed",
  "comments": "This scheduled payment series is to pay for the thing."
}
```

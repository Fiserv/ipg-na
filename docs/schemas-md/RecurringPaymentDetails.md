
# RecurringPaymentDetailsResponse

| *description*:   | *Details about existing gateway schedule.*|
|----|----|
| storeId |    ``` string ```  *example:   30dd879c-ee2f-11db-8314-0800200c9a66*. Store ID number.|
| purchaseOrderNumber |    ``` string ```  *example: 123055342*. Purchase order number.|
| invoiceNumber |    ``` string ```  *example: 96126098*. Invoice number.|
| | additionalDetails |  |  
| creationDate |    ``` string ```  *example: Tue Jul 14 13:40:26 IST 2020*.  Deprecated. Please use creationDateFormatted. This may be removed in a future release. Date recurring payment was created.|
| startDate |    ``` string ```  *example: Tue Jul 14 13:40:26 IST 2020*.  Deprecated. Please use startDateFormatted. This may be removed in a future release. Date of mandate signature.|
| nextAttemptDate |    ``` string ```  *example:  Tue Jul 14 13:40:26 IST 2020*. Deprecated. Please use nextAttemptDateFormatted. This may be removed in a future release. Date of next transaction process attempt.|
| creationDateFormatted |    ``` string ```  *example: 2018-10-25*. Date recurring payment was created.|
| startDateFormatted |    ``` string ```  *example: 2018-10-25*. Date of mandate signature.|
| nextAttemptDateFormatted |    ``` string ```  *example: 2018-10-25*. Date of next transaction process attempt.
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| paymentMethodDetails |   |
| frequency |   |
| numberOfPayments |    ``` integer ``` ($int32)  *minimum: 1 maximum: 999 example: 10*. Number of times the recurring payment will process.|
| runCount |    ``` integer ``` ($int32)  *minimum: 0 maximum: 999 example: 10*. Times the recurring payment has already run.|
| state | RecurringPaymentState   ``` string ```  *example: Installed*. Installed. Enum:Array [ 3 ] - [ Installed, Inactivated, Cancelled ]|
| comments |    ``` string ```  *example: This scheduled payment series is to pay for the thing.*. User supplied comments.|  

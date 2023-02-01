
# ProcessorData

| *description*:   | *Model for processor data.*|
|----|----|
| referenceNumber |    ``` string ```  *example: 811720726601*. Reference transaction ID.|
| authorizationCode |    ``` string ```  *example: OK7118*. Code returned to confirm transaction.|
| responseCode |   ``` string ```  *example: 00*. Response code from endpoints.|
| network |   ``` string ```  *example: NYCE*. Network used for transaction.|
| associationResponseCode |   ``` string ```  *example: 00*. Raw response code from issuer.
| responseMessage |   ``` string ```  *example: Amount specified exceeds allowable limit*. Message returned from endpoints.|
| avsResponse |   | 
| cardholderInfoResponse |   |
| securityCodeResponse |   ``` string ```  *example: NOT_MATCHED*. Code returned for CVV. Enum:Array [ 6 ] - [ MATCHED, NOT_MATCHED, NOT_PROCESSED, NOT_PRESENT, NOT_CERTIFIED, NOT_CHECKED ]|
| merchantAdviceCodeIndicator |   ``` string ```  *pattern: [0-9]{2}  example: 01*. Code to map merchant advice code to ISO specification.|
| responseIndicator |   ``` string ```  *example:0100*.Indicates whether the transaction was routed through the payment card's own network or through a different network.|
| debitReceiptNumber |   ``` string ```  *example:123456*.Receipt number from debit network provider.|
| transactionIntegrityClass |   ``` string ```  *example:A1*. MasterCard provided Transaction Integrity Class for Point of Sale (POS) Purchase and Purchase with Cash Back transactions initiated on the Authorization Platform.|   

**ProcessorData Example:**

```{r}

{
  "responseCode": "00",
  "responseMessage": "APPROVED",
  "authorizationCode": "OK7118",
  "network": "NYCE"
}
```


  


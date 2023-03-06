
# ProcessorData

| *description*:   | *Model for processor data.*|
|----|----|
| referenceNumber |    ``` string ```  <br/>  *example: 811720726601* <br/>  Reference transaction ID.|
| authorizationCode |    ``` string ```  <br/>  *example: OK7118* <br/>  Code returned to confirm transaction.|
| responseCode |   ``` string ``` <br/>   *example: 00* <br/> Response code from endpoints.|
| network |   ``` string ```   <br/> *example: NYCE* <br/> Network used for transaction.|
| associationResponseCode |   ``` string ```  <br/>  *example: 00* <br/>  Raw response code from issuer.
| responseMessage |   ``` string ``` <br/>  *example: Amount specified exceeds allowable limit* <br/>  Message returned from endpoints.|
| avsResponse |  [AVSResponse](?path=docs/schemas-md/AVSResponse.md)| 
| cardholderInfoResponse | [cardholderInfoResponse](?path=docs/schemas-md/CardholderInfoResponse.md)|
| securityCodeResponse |   ``` string ```  <br/>  *example: NOT_MATCHED* <br/> Code returned for CVV.  <br/> Enum:Array [ 6 ] - [ MATCHED, NOT_MATCHED, NOT_PROCESSED, NOT_PRESENT, NOT_CERTIFIED, NOT_CHECKED ]|
| merchantAdviceCodeIndicator |   ``` string ```  <br/>  pattern: [0-9]{2}  <br/>  *example: 01* <br/> Code to map merchant advice code to ISO specification.|
| responseIndicator |   ``` string ```  <br/>  *example:0100* <br/> Indicates whether the transaction was routed through the payment card's own network or through a different network.|
| debitReceiptNumber |   ``` string ```  <br/> *example:123456* <br/> Receipt number from debit network provider.|
| transactionIntegrityClass |   ``` string ```  <br/> *example:A1* <br/> MasterCard provided Transaction Integrity Class for Point of Sale (POS) Purchase and Purchase with Cash Back transactions initiated on the Authorization Platform.|   

**ProcessorData Example:**

```{r}

{
  "responseCode": "00",
  "responseMessage": "APPROVED",
  "authorizationCode": "OK7118",
  "network": "NYCE"
}
```


  


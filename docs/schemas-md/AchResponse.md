
# AchResponse

| *description*:   | *ACH TeleCheck response.*|
|----|----|
| responseCode |    ``` string ```   <br/> *maxLength: 2 example: 49* <br/>  Response code for TeleCheck authentication decision in the sale response message.|
| approvalCode |    ``` string ```   <br/> *maxLength: 4 example: A123* <br/>  Code provided if check is approved.|
| referenceNumber |    ``` string ```  <br/>  *example: 1234567* <br/>  Reference number.|
| preferredFlag |    ``` string ```   <br/> maxLength: 1  <br/> *example: Y* <br/>  Preferred flag.|
| transactionStatus |    ``` string ```   <br/> maxLength: 1  <br/> *example: 1*  <br/> Indicates the result of the requested authorization and is returned in the sale response.|

**AchResponse Example:**

```{r}

{
  "responseCode": "49",
  "approvalCode": "ASF2",
  "referenceNumber": "1234567",
  "preferredFlag": "Y",
  "transactionStatus": "1"
}
```  
  


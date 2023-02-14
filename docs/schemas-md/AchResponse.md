
# AchResponse

| *description*:   | *ACH TeleCheck response.*|
|----|----|
| responseCode |    ``` string ```  *maxLength: 2 example: 49* Response code for TeleCheck authentication decision in the sale response message.|
| approvalCode |    ``` string ```  *maxLength: 4 example: A123* Code provided if check is approved.|
| referenceNumber |    ``` string ```  *example: 1234567* Reference number.|
| preferredFlag |    ``` string ```  *maxLength: 1 example: Y* Preferred flag.|
| transactionStatus |    ``` string ```  *maxLength: 1 example: 1* Indicates the result of the requested authorization and is returned in the sale response.|

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
  



# AccountUpdaterResponse

| *description*:   | *Details related to updated account information.*|
|----|----|
| updatedCard |    ``` string ```  *example: 4012000066660018* Account updater replacement PAN or TransArmor token.|
| updatedToken |    ``` string ```  *example: 1235325235236* Updated value of token.|
| updatedExpirationDate |    ``` string ```  *example: 1220* New account number expiration date in MMYY format.|
| updatedAccountStatus |    ``` string ```  *example: ACCOUNT_CHANGED* Status of the updated account. An account may have closed (ACCOUNT_CLOSED), the expiry date may have changed (EXPIRY_CHANGED), the account may have changed (ACCOUNT_CHANGED), or the cardholder should be contacted (CONTACT_CARDHOLDER).|
| updatedAccountErrorCode |    ``` string ```  *example: VAU002* Code for the error encountered when updating account.|
| originalResponseCode |    ``` string ```  *example: 00* Original Response Code for re-authorized (Optimized) transaction.|  


**AccountUpdaterResponse Example:**

```{r}

{
  "updatedCard": "4012000066660018",
  "updatedExpirationDate": "1220",
  "updatedAccountStatus": "ACCOUNT_CHANGED",
  "updatedAccountErrorCode": "VAU002",
  "originalResponseCode": "00"
}
```  
 

  








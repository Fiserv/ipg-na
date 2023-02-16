
# AccountUpdaterResponse

| *description*:   | *Details related to updated account information.*|
|----|----|
| updatedCard |    ``` string ```   <br/> *example: 4012000066660018*  <br/> Account updater replacement PAN or TransArmor token.|
| updatedToken |    ``` string ```   <br/> *example: 1235325235236*  <br/> Updated value of token.|
| updatedExpirationDate |    ``` string ```   <br/> *example: 1220*  <br/> New account number expiration date in MMYY format.|
| updatedAccountStatus |    ``` string ```   <br/> *example: ACCOUNT_CHANGED*  <br/> Status of the updated account. An account may have closed (ACCOUNT_CLOSED), the expiry date may have changed (EXPIRY_CHANGED),  <br/> the account may have changed (ACCOUNT_CHANGED), or the cardholder should be contacted (CONTACT_CARDHOLDER).|
| updatedAccountErrorCode |    ``` string ```  <br/>  *example: VAU002* <br/>  Code for the error encountered when updating account.|
| originalResponseCode |    ``` string ```  <br/>  *example: 00*  <br/> Original Response Code for re-authorized (Optimized) transaction.|  


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
 

  








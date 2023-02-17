
# DecryptedGooglePay

| *description*:   | *Decrypted Google Pay payload.*|
|----|----|
| accountNumber* |    ``` string ```  <br/>  *pattern: [0-9]{13,19} example: 4111111111111111*  <br/> Payment card number.|
| expiration* |     ``` string ```  <br/>  *pattern: [0-9]{6}  <br/> example: 012040*  <br/> Card expiration date in MMYYYY format.| 
| cardholderName |    ``` string ``` <br/>   *maxLength: 96 pattern: ^(?!\s*$).+  <br/> example: John Doe* <br/>  Name of the cardholder.|
| brand |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+  <br/> example: VISA*  <br/> Card brand.|
| cryptogram* |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+  <br/> example: BB81SRsADvooHCUcDogjMAACAAA=*  <br/> The wallet cryptogram from the decrypted data.|
| eciIndicator |    ``` string ```  *pattern: [0-9]{2}  <br/> example: 05*  <br/> The ECI indicator from the decrypted data.|
| storedCredentials | [StoredCredentials](?path=docs/schemas-md/StoredCredentials.md)| 

**DecryptedGooglePay Example:**

```{r}

{
  "accountNumber": "4111111111111111",
  "expiration": "221201",
  "cardholderName": "John Doe",
  "brand": "VISA",
  "cryptogram": "BB81SRsADvooHCUcDogjMAACAAA=",
  "eciIndicator": "05",
  "storedCredentials": {
    "sequence": "FIRST",
    "scheduled": false,
    "referencedSchemeTransactionId": "019087868716215",
    "initiator": "CARDHOLDER"
  }
}
``` 





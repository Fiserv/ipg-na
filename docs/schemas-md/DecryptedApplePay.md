
# DecryptedApplePay

| *description*:   | *Decrypted Apple Pay payload.*|
|----|----|
| accountNumber* |    ``` string ``` <br/> *pattern: [0-9]{13,19} example: 4111111111111111*  <br/> Payment card number.|
| expiration* |     ``` string ```   <br/> *pattern: [0-9]{6} example: 012040* <br/>  Card expiration date in MMYYYY format.| 
| cardholderName |    ``` string ```  <br/>  *maxLength: 96 pattern: ^(?!\s*$).+ example: John Doe*  <br/> Name of the cardholder.|
| brand |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+ example: VISA* <br/>  Card brand.|
| cryptogram* |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+ example: BB81SRsADvooHCUcDogjMAACAAA=* <br/>  The wallet cryptogram from the decrypted data.|
| eciIndicator |    ``` string ```  <br/>  *pattern: [0-9]{2} example: 05*  <br/> The ECI indicator from the decrypted data.|

**DecryptedApplePay Example:**

```{r}

{
  "accountNumber": "4111111111111111",
  "expiration": "221201",
  "cardholderName": "John Doe",
  "brand": "VISA",
  "cryptogram": "BB81SRsADvooHCUcDogjMAACAAA=",
  "eciIndicator": "05"
}
``` 





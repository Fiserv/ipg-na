
# DecryptedSamsungPay

| *description*:   | *Decrypted Samsung Pay payload.*|
|----|----|
| accountNumber* |    ``` string ```  *pattern: [0-9]{13,19} example: 4111111111111111* Payment card number.|
| expiration* |     ``` string ```  *pattern: [0-9]{6} example: 012040* Card expiration date in MMYYYY format.| 
| cardholderName |    ``` string ```  *maxLength: 96 pattern: ^(?!\s*$).+ example: John Doe* Name of the cardholder.|
| brand |    ``` string ```  *pattern: ^(?!\s*$).+ example: VISA* Card brand.|
| cryptogram* |    ``` string ```  *pattern: ^(?!\s*$).+ example: BB81SRsADvooHCUcDogjMAACAAA=* The wallet cryptogram from the decrypted data.|
| eciIndicator |    ``` string ```  *pattern: [0-9]{2} example: 05* The ECI indicator from the decrypted data.|

**DecryptedSamsungPay Example:**

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






# EncryptedGooglePay

| *description*:   | *Encrypted Google Pay payload.*|
|----|----|
| data* |    ``` string ```  *pattern: ^(?!\s*$).+ example: NdCmVw5nMjQq746HYc/VbiZcQZ/zFzeEcM1wVMPruEG4/C/EFhobSkwB5JZJU+t6JuDVXUBiRYuOOC8FTYd+qIm6ckktid9aiGh0f2NDP0INSr59QXmr389RonyUfRYKnBmwsh5UqtI7Iz0AmMtl1PWMdxcCewtjuffs79ahTnFgXsRN+ynuhyDfbdRanlTnYKGoTeVh9eJfheJ1wquO+jiGj+npJ/Oh9bAdlw7iEHrYO2aUkgaMyXZ3foXRAJeimQVQS1y8lU1PPq62zpPrFzidbnnU5fK25pvGFjOdmLsBELZPk5thQEkSaA9p1LSKzWSesHhi0BxZaFPXSA6ANXvYIU2AT0lG+0O0w1URA5Sinyj3YDZVqjuir6rzNN9bB2U2nTQnKMbuGLMS20K8fUKZN/YLJh+AtE6J69+VVSU95mE1nOb8hyabz6E5RmnC5Ze2k6F/hQ75ig==* The encrypted wallet payload.|
| signature* |    ``` string ```  *pattern: ^(?!\s*$).+ example: MIAGCSqGSIb3DQEHAqCAMIACAQExDzANBglghkgBZQMEAgEFADCABgkqhkiG9w0BBwEAAKCAMIIB0zCCAXkCAQEwCQYHKoZIzj0EATB2MQswCQYDVQQGEwJVUzELMAkGA1UECAwCTkoxFDASBgNVBAcMC0plcnNleSBDaXR5MRMwEQYDVQQKDApGaXJzdCBEYXRhMRIwEAYDVQQLDAlGaXJzdCBBUEkxGzAZBgNVBAMMEmQxZHZ0bDEwMDAuMWRjLmNvbTAeFw0xNTA3MjMxNjQxMDNaFw0xOTA3MjIxNjQxMDNaMHYxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJOSjEUMBIGA1UEBwwLSmVyc2V5IENpdHkxEzARBgNVBAoMCkZpcnN0IERhdGExEjAQBgNVBAsMCUZpcnN0IEFQSTEbMBkGA1UEAwwSZDFkdnRsMTAwMC4xZGMuY29tMFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAErnHhPM18HFbOomJMUiLiPL7nrJuWvfPy0Gg3xsX3m8q0oWhTs1QcQDTT+TR3yh4sDRPqXnsTUwcvbrCOzdUEeTAJBgcqhkjOPQQBA0kAMEYCIQDrC1z2JTx1jZPvllpnkxPEzBGk9BhTCkEB58j/Cv+sXQIhAKGongoz++3tJroo1GxnwvzK/Qmc4P1K2lHoh9biZeNhAAAxggFUMIIBUAIBATB7MHYxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJOSjEUMBIGA1UEBwwLSmVyc2V5IENpdHkxEzARBgNVBAoMCkZpcnN0IERhdGExEjAQBgNVBAsMCUZpcnN0IEFQSTEbMBkGA1UEAwwSZDFkdnRsMTAwMC4xZGMuY29tAgEBMA0GCWCGSAFlAwQCAQUAoGkwGAYJKoZIhvcNAQkDMQsGCSqGSIb3DQEHATAcBgkqhkiG9w0BCQUxDxcNMTUwODEyMTczMTAwWjAvBgkqhkiG9w0BCQQxIgQgJyjKLiGQo3I1ZbfHSmF2XCZ8dNlcZyohziuXO48EKwgwCgYIKoZIzj0EAwIESDBGAiEAznKDYEz9MsC+r1g6e4LR1DTaQOl+X2rVNkWnKDpc1EQCIQCmK48ChHoz4HWnUnW5XqaGWOUXKHQvUgeqFr/jgBUzegAAAAAAAA==* Signature of the payment and header data.|
| version |    ``` string ```  *example: EC_v1* Version information about the payment token. Enum:[ EC_v1 ]|

**EncryptedGooglePay Example:**

```{r}

{
   "amount":{
      "total": 12.04,
      "currency": "USD"
   },
   "source":{
      "sourceType": "GooglePay",
      "data": "{\"encryptedMessage\":\"NZF5Vs2YaI\/t25L\/1+dp6tuUOvra9pszs2antqcbHJbkjMMXZSR7innTFJxNR5DNnf4GheWIso8n8MA1q1zqWCU8MaK9bnNcHxvROpvfsU3SCCjkfG2k2M4\/RYMjs+lxYW\/nEtIIKVVOkdjAj4pI\/Wth8xQXphn7hDNiyp9tIydmlPZVnzkXI6mVbpHbbkaCCD4TNPhFBDtx0VafqRjbb2Wt3EDazTx3dHdd+qVX5Xj8\/BPb1cmwHWvrDw\/dQRk\/E0TsP+erLjhLaZ8l2EycxeUEZYqSX5w77S8vd3sw8WXuOCMsU8sx0Bs5IY7hohq67qNDxckP1fcBD4OYdGP6bumJR0J6pJxD5iRh5lFSjN6zNLRI77ylxWL6DwHoe\/pPdCc0n6cV0Nt0RJMLjerr12BLuhv4bPQ3QB6jxnbt8JK\/EndgIG8xpFyNkKlRUyxAKM22\/ZSy45d6qtZIKLXRqDTr9JMk8uJ53QRZtQx8k9KkRZGC+GM2sD+Z75fxc0Yye7l6H0D8p5z1iEzWnYHxd0pmY\/cOYEJxnOOdD573QmE6ikFcyaAw3XnCyul\/EA\\u003d\\u003d\",\"ephemeralPublicKey\":\"BAhnPIWrCXWv\/45GFK0mNAvN9w+NFBs3tQji0wTUS2+hiFKsZujG5wRd4JXGmxhG+k3bglYk544ILBNdDpsAh+o\\u003d\",\"tag\":\"liBzKfGcO+FclHg7XuqRJxR\/8EJShRp9\/APab0Sho08\\u003d\"}",
      "signature": "MIAGCSqGSIb3DQEHAqCAMIACAQExDzAN...",
      "version": "ECv2"
   },
   "transactionDetails":{
      "captureFlag": true,
      "createToken": false
   },
   "merchantDetails":{
      "merchantId": "123456789789567",
      "terminalId": "123456"
   }
}
``` 





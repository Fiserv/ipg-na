
# EncryptedApplePay

| *description*:   | *Encrypted Apple Pay payload.*|
|----|----|
| data* |    ``` string ```  *pattern: ^(?!\s*$).+ example: NdCmVw5nMjQq746HYc/VbiZcQZ/zFzeEcM1wVMPruEG4/C/EFhobSkwB5JZJU+t6JuDVXUBiRYuOOC8FTYd+qIm6ckktid9aiGh0f2NDP0INSr59QXmr389RonyUfRYKnBmwsh5UqtI7Iz0AmMtl1PWMdxcCewtjuffs79ahTnFgXsRN+ynuhyDfbdRanlTnYKGoTeVh9eJfheJ1wquO+jiGj+npJ/Oh9bAdlw7iEHrYO2aUkgaMyXZ3foXRAJeimQVQS1y8lU1PPq62zpPrFzidbnnU5fK25pvGFjOdmLsBELZPk5thQEkSaA9p1LSKzWSesHhi0BxZaFPXSA6ANXvYIU2AT0lG+0O0w1URA5Sinyj3YDZVqjuir6rzNN9bB2U2nTQnKMbuGLMS20K8fUKZN/YLJh+AtE6J69+VVSU95mE1nOb8hyabz6E5RmnC5Ze2k6F/hQ75ig==* The encrypted wallet payload.|
| header* | { [header](?path=docs/schemas-md/Header.md) }| 
| signature* |    ``` string ```  *pattern: ^(?!\s*$).+ example: MIAGCSqGSIb3DQEHAqCAMIACAQExDzANBglghkgBZQMEAgEFADCABgkqhkiG9w0BBwEAAKCAMIIB0zCCAXkCAQEwCQYHKoZIzj0EATB2MQswCQYDVQQGEwJVUzELMAkGA1UECAwCTkoxFDASBgNVBAcMC0plcnNleSBDaXR5MRMwEQYDVQQKDApGaXJzdCBEYXRhMRIwEAYDVQQLDAlGaXJzdCBBUEkxGzAZBgNVBAMMEmQxZHZ0bDEwMDAuMWRjLmNvbTAeFw0xNTA3MjMxNjQxMDNaFw0xOTA3MjIxNjQxMDNaMHYxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJOSjEUMBIGA1UEBwwLSmVyc2V5IENpdHkxEzARBgNVBAoMCkZpcnN0IERhdGExEjAQBgNVBAsMCUZpcnN0IEFQSTEbMBkGA1UEAwwSZDFkdnRsMTAwMC4xZGMuY29tMFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAErnHhPM18HFbOomJMUiLiPL7nrJuWvfPy0Gg3xsX3m8q0oWhTs1QcQDTT+TR3yh4sDRPqXnsTUwcvbrCOzdUEeTAJBgcqhkjOPQQBA0kAMEYCIQDrC1z2JTx1jZPvllpnkxPEzBGk9BhTCkEB58j/Cv+sXQIhAKGongoz++3tJroo1GxnwvzK/Qmc4P1K2lHoh9biZeNhAAAxggFUMIIBUAIBATB7MHYxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJOSjEUMBIGA1UEBwwLSmVyc2V5IENpdHkxEzARBgNVBAoMCkZpcnN0IERhdGExEjAQBgNVBAsMCUZpcnN0IEFQSTEbMBkGA1UEAwwSZDFkdnRsMTAwMC4xZGMuY29tAgEBMA0GCWCGSAFlAwQCAQUAoGkwGAYJKoZIhvcNAQkDMQsGCSqGSIb3DQEHATAcBgkqhkiG9w0BCQUxDxcNMTUwODEyMTczMTAwWjAvBgkqhkiG9w0BCQQxIgQgJyjKLiGQo3I1ZbfHSmF2XCZ8dNlcZyohziuXO48EKwgwCgYIKoZIzj0EAwIESDBGAiEAznKDYEz9MsC+r1g6e4LR1DTaQOl+X2rVNkWnKDpc1EQCIQCmK48ChHoz4HWnUnW5XqaGWOUXKHQvUgeqFr/jgBUzegAAAAAAAA==* Signature of the payment and header data.|
| version |    ``` string ```  *example: EC_v1* Version information about the payment token. Enum:[ EC_v1 ]|
| applicationData |    ``` string ```  *example: VEVTVA==* Base64-encoded value of PKPaymentRequest. Required only if applicationDataHash is present.|
| merchantId* |    ``` string ```  *pattern: ^(?!\s*$).+ example: order-1* The merchant ID assigned by the wallet provider.|

**EncryptedApplePay Example:**

```{r}

{
  "data": {
    "encryptedMessage": "8nxjB9mr2tWZeDRQRcGN91UUnb7AioGp3oRo8kmQ6lyvJZiqD7PJlbRCYElNqUmr6Z8zK7b2gO9MKOjpnTCqH0qAe2vuIlwNXB60M2Lh7Qfl3bVgWzwF/FfFcenVW381hoItYi8AjWnWoydz1XMTEv2qhqUG03mEnRXdMyDyk6KKZXoW8Qc0p1F1thbxxu8weU8CZbZsWGGTjB42cilIqLVbribcOAG8Oas1AcgefFsu2hwp4gdSuOg7wmeSV7XKsGQzzVy85qtjuqET2XYzJE3K/Wh9QKkhu5P9Ms5s1+Smr2IjRyidqQa88SxQplrVoo9+PvT0bxFcMspBmO3pLkuaZSUBy++dL2fefcxNJvGCFfFhdxW9DojuuQxgpeu7RAQUsGLyFmr/4ZfBxt882xTmpX9MRx5CAudl9qUgBfKdwWwMX35qSbDTm1ju5XXzNh94VebjD3bB9Zj8qgbmUOr/+6OQLhoFJyBCXgx3EEH8hBwNVFrss/SLwQvFhZh62eO6lOtnmbOtP1yTDDVqGDBfai5SwAmM+KTcc9SGv/xDC+cWe8ck+aCBkG4HoRPapUVMZ3JIgV7yzTsVLJE\\\\u003d\\\\",
    "ephemeralPublicKey": "BGH3fRFdoAobYrAlxnZOCYzkH84Cna92IZxtgsU36CMDaqSaDYb9/LsY8qw+vMtlBnwsUg/YVMOeeKp+qDkOWb4\\\\u003d\\\\",
    "tag": "nvmOUNpnOTZULLhMxT/hWCHzH/4f7gGpfvQgwl3p8ng\\\\u003d\\\\"
  },
  "signature": "MEUCIFWTRWUZAOM5nfJC79FtJm56olnbwG4H5uWWxAUWAquiAiEA24j/BcOroeISsdJzYsyoVi8wzu4tnmKw+jdsGfuvPko=",
  "version": "ECv1"
}
``` 





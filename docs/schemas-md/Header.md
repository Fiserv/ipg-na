

| *description*:   | *Additional version-dependent information used to decrypt and verify the payment.*|
|----|----|
| applicationDataHash |    ``` string ``` <br/>  *example: 94ee059335e587e501cc4bf90613e0814f00a7b08bc7c648fd865a2af6a22cc2* <br/>  Merchant supplied information about the payment request. Contains Base64-encoded SHA256 hash of the applicationData property of the original PKPaymentRequest.  <br/> Note - applicationData from PaymentData of PKPaymentToken Refer to Apple Pay documentation.|
| ephemeralPublicKey* |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+  <br/> example: MFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAEiaU1SbkYTJy/j5L1t51vtGDh4KlNl5MFPWzo/C8r0WcrktWriz5pdRaDVUDvU++KlDu2iuQsd2xSNKJlFscbDQ==*  <br/> Temporary key for generating shared secret from a device.|
| publicKeyHash* |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+  <br/> example: YmSWN7lj4+A6fVJVPicP8TgS7gI7ougD8rEWB5LXtMM=*  <br/>  Hash of the X.509 encoded public key bytes of the merchant’s certificate.|
| transactionId* |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+  <br/> example: 31323334353637*  <br/> Transaction identifier, generated on the device.
|
| publicKeyHash* |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+  <br/> example: YmSWN7lj4+A6fVJVPicP8TgS7gI7ougD8rEWB5LXtMM=*   <br/> Hash of the X.509 encoded public key bytes of the merchant’s certificate.|
   


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





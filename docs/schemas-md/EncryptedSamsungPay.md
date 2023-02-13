
# EncryptedSamsungPay

| *description*:   | *Encrypted Samsung Pay payload.*|
|----|----|
| data* |    ``` string ```  *pattern: ^(?!\s*$).+ example: 8nxjB9mr2tWZeDRQRcGN91UUnb7AioGp3oRo8kmQ6lyvJZiqD7PJlbRCYElNqUmr6Z8zK7b2gO9MKOjpnTCqH0qAe2vuIlwNXB60M2Lh7Qfl3bVgWzwF/FfFcenVW381hoItYi8AjWnWoydz1XMTEv2qhqUG03mEnRXdMyDyk6KKZXoW8Qc0p1F1thbxxu8weU8CZbZsWGGTjB42cilIqLVbribcOAG8Oas1AcgefFsu2hwp4gdSuOg7wmeSV7XKsGQzzVy85qtjuqET2XYzJE3K/Wh9QKkhu5P9Ms5s1+Smr2IjRyidqQa88SxQplrVoo9+PvT0bxFcMspBmO3pLkuaZSUBy++dL2fefcxNJvGCFfFhdxW9DojuuQxgpeu7RAQUsGLyFmr/4ZfBxt882xTmpX9MRx5CAudl9qUgBfKdwWwMX35qSbDTm1ju5XXzNh94VebjD3bB9Zj8qgbmUOr/+6OQLhoFJyBCXgx3EEH8hBwNVFrss/SLwQvFhZh62eO6lOtnmbOtP1yTDDVqGDBfai5SwAmM+KTcc9SGv/xDC+cWe8ck+aCBkG4HoRPapUVMZ3JIgV7yzTsVLJE\\u003d\\* The encrypted wallet payload.|
| version |    ``` string ```  *pattern: ^(?!\s*$).+ example: 100* Identifies under which encryption/signing scheme this message has been created. In this way, the protocol can evolve over time if needed. For Google Payments transactions, this should be set to ECv1. 
| applicationData |    ``` string ```  *example: VEVTVA==* Base64-encoded value of PKPaymentRequest. Required only if applicationDataHash is present.|

**EncryptedSamsungPay Example:**

```{r}

{
  "data": "eyJhbGciOiJSU0ExXzUiLCJraWQiOiJadDRZQ0dpRVMvU2F0RGtuampsdnhxNmdNUTRDK1lvcFJUanJtTDBlRldZPSIsInR5cCI6IkpPU0UiLCJjaGFubmVsU2VjdXJpdHlDb250ZXh0IjoiUlNBX1BLSSIsImVuYyI6IkExMjhHQ00ifQ",
  "version": "100"
}
``` 





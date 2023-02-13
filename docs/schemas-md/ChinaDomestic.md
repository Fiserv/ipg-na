
# ChinaDomestic

| *description*:   | *The payment object for China-domestic transactions. Use this to populate all china domestic payment method details.*|
|----|----|
| productCode* |    ``` string ```   *maxLength: 32 pattern: ^(?!\s*$).+ example: R2D2C3PO* Use this to indicate the product code according to the product category list.|
| productQuantity* |    ``` integer ```   *minimum: 1 example: 10* The quantity.|
| productPrice* |    ``` number ```   *example: 3.2 Rate amount in 3 decimal 12 bytes total digit.|
| productDescription*	 |    ``` string ```   *maxLength: 100 pattern: ^(?!\s*$).+ example: Best product ever* The product description.|
| redirectURL* |    ``` string ```   *maxLength: 1024 pattern: ^(?!\s*$).+ example: www.urlredirectedto.com* Use this to indicate the product code according to the product category list.|
| limitCardFunctionToDebit*	 |    ``` boolean ```   *example: true* Use this to limit card functions to debit cards.|
| customerId |    ``` string ```   *maxLength: 32 example: ID3Bs Use this to indicate the CUP customer ID if known.|
| bankId |    ``` string ```   *maxLength: 8 example: 123456* Use this to indicate the CUP bank ID if known.|
| openId |    ``` string ```   *maxLength: 128 example: op5EP1G8XtyYH1VvmAbleB3AYgc8* Use this as unique identifier of WeChat user which is corresponded to the appid of merchant. The field is only applicable for ChinaDomesticPaymentMethod - brand = WECHAT_DOMESTIC|

**ChinaDomestic Example:**

```{r}

{
  "productCode": "R2D2C3PO",
  "productQuantity": 10,
  "productPrice": 3.2,
  "productDescription": "Best product ever",
  "redirectURL": "www.urlredirectedto.com",
  "limitCardFunctionToDebit": true,
  "customerId": "ID3Bs",
  "bankId": "123456"
}
```






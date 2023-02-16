
# ChinaDomestic

| *description*:   | *The payment object for China-domestic transactions. Use this to populate all china domestic payment method details.*|
|----|----|
| productCode* |    ``` string ```   <br/> maxLength: 32 <br/>  pattern: ^(?!\s*$).+  <br/> *example: R2D2C3PO*  <br/> Use this to indicate the product code according to the product category list.|
| productQuantity* |    ``` integer ```    <br/> minimum: 1  <br/> *example: 10*  <br/> The quantity.|
| productPrice* |    ``` number ```   *example: 3.2 Rate amount in 3 decimal 12 bytes total digit.|
| productDescription*	 |    ``` string ```  <br/> maxLength: 100  <br/> pattern: ^(?!\s*$).+  <br/> *example: Best product ever*  <br/> The product description.|
| redirectURL* |    ``` string ```    <br/> maxLength: 1024  <br/> pattern: ^(?!\s*$).+  <br/> *example: www.urlredirectedto.com*  <br/> Use this to indicate the product code according to the product category list.|
| limitCardFunctionToDebit*	 |    ``` boolean ```  <br/>   *example: true*  <br/> Use this to limit card functions to debit cards.|
| customerId |    ``` string ```  <br/> maxLength: 32  <br/> *example: ID3Bs*   <br/> Use this to indicate the CUP customer ID if known.|
| bankId |    ``` string ```    <br/> maxLength: 8  <br/> *example: 123456*  <br/> Use this to indicate the CUP bank ID if known.|
| openId |    ``` string ```    <br/> maxLength: 128  <br/> *example: op5EP1G8XtyYH1VvmAbleB3AYgc8*  <br/> Use this as unique identifier of WeChat user which is corresponded to the appid of merchant.  <br/> The field is only applicable for ChinaDomesticPaymentMethod - brand = WECHAT_DOMESTIC|

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






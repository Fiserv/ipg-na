
# ChinaDomesticPaymentMethod

| *description*:   | *Payment method containing China Domestic information.*|
|----|----|
| chinaDomestic* |  [ChinaDomestic](?path=docs/schemas-md/ChinaDomestic.md)|
| brand* |    ``` string ```  <br/>   Enum:Array [ 3 ] - [ ALIPAY_DOMESTIC, CUP_DOMESTIC, WECHAT_DOMESTIC ]|

**ChinaDomesticPaymentMethod Example:**

```{r}

{
  "chinaDomestic": {
    "productCode": "R2D2C3PO",
    "productQuantity": 10,
    "productPrice": 3.2,
    "productDescription": "Best product ever",
    "redirectURL": "www.urlredirectedto.com",
    "limitCardFunctionToDebit": true,
    "customerId": "ID3Bs",
    "bankId": "123456"
  },
  "brand": "CUP_DOMESTIC"
}
```




# CreatePaymentToken

| *description*:   | *Use this model to create a payment token.*|
|----|----|
| value |    ``` string ```  <br/>  *example:  234ljl124l12*.  <br/> Client-supplied payment token value. Only applicable for DataVault tokenization scheme.|
| reusable |    ``` boolean ```  <br/> default: true   <br/> *example: true*.  <br/> If the token is reusable.|
| declineDuplicates |    ``` boolean ```  <br/> default: false   <br/> *example: false*.  <br/> Decline duplicate payment info if client token is supplied.|   

**CreatePaymentToken Example:**

```{r}
{
  "value": "234ljl124l12",
  "reusable": true,
  "declineDuplicates": false
}
```
 
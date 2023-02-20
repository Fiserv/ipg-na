
# LineItems

| *description*: | *Level3 - lineItems*|
|----|----|
| commodityCode |    ``` string ```  <br/>   *example: ab12* <br/>  Commodity Code.|
| productCode |    ``` string ```  <br/>   *example: 0001212120888* <br/>  Product Code|
| description |    ``` string ```  <br/>   *maxLength: 4 <br/>  example: Dinner and movie*  <br/> Description of the line item.|
| quantity |    ``` number ```   <br/>  *example: 5*  <br/> Quantity.|
| unitMeasure |    ``` number ```  <br/>   *example: 25*  <br/> Number of units.|
| unitPrice |    ``` number ```   <br/>  *example: 30.075*  <br/> Unit Price.|
| vatAmountAndRate | [AdditionalAmountRate](?path=docs/schemas-md/AdditionalAmountRate.md)|
| discountAmountAndRate | [AdditionalAmountRate](?path=docs/schemas-md/AdditionalAmountRate.md)|

**LineItems Example:**

```{r}

{
     "commodityCode": "ab12",
     "productCode": "0001212120888",
     "description": "Dinner and movie",
     "quantity": 5,
     "unitMeasure": "25",
     "unitPrice": 30.075,
     "vatAmountAndRate": {
     "amount": 5.145,
     "rate": 1.175
     },
     "discountAmountAndRate": {
        "amount": 6.03,
        "rate": 1.175
     },
     "lineItemTotal": 39.075
}
```  







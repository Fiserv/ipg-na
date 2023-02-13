
# LineItems

| *description*: | *Level3 - lineItems*|
|----|----|
| commodityCode |    ``` string ```   *example: ab12* Commodity Code.|
| productCode |    ``` string ```   *example: 0001212120888* Product Code|
| description |    ``` string ```   *maxLength: 4 example: Dinner and movie* Description of the line item.|
| quantity |    ``` number ```   *example: 5* Quantity.|
| unitMeasure |    ``` number ```   *example: 25* Number of units.|
| unitPrice |    ``` number ```   *example: 30.075* Unit Price.|
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







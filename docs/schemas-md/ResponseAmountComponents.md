
# ResponseAmountComponents

| *description*:   | *Amount component details, used in responses.*|
|----|----|
| subtotal* |    ``` number ```   <br/>  *example: 8* <br/>  Subtotal amount.|
| vatAmount |    ``` number ```  <br/>   *example: 0* <br/>  Value-added tax amount.|
| localTax |    ``` number ```  <br/>   *example: 1* <br/>  Local tax amount.|
| shipping |    ``` number ```  <br/>   *example: 1.24* <br/>  Shipping amount.|
| cashback |    ``` number ```  <br/>   *example: 2* <br/>  Cashback amount.|
| tip |    ``` number ```   <br/>  *example: 6*. <br/>  Tip amount.|
| surcharge |    ``` number ```  <br/>   *example: 2.5* <br/>  Surcharge  amount.|
| convenienceFee |    ``` number ```   <br/>  *example: 2.5* <br/>  Amount added for proccessing or handling fees.|   

**ResponseAmountComponents Example:**

```{r}

{
  "subtotal": 8,
  "vatAmount": 0,
  "localTax": 1.3,
  "convenienceFee": 2
}
```  






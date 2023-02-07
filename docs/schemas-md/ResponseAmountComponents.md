
# ResponseAmountComponents

| *description*:   | *Amount component details, used in responses.*|
|----|----|
| subtotal* |    ``` number ```   *example: 8*. Subtotal amount.|
| vatAmount |    ``` number ```   *example: 0*. Value-added tax amount.|
| localTax |    ``` number ```   *example: 1*. Local tax amount.|
| shipping |    ``` number ```   *example: 1.24*. Shipping amount.|
| cashback |    ``` number ```   *example: 2*. Cashback amount.|
| tip |    ``` number ```   *example: 6*. Tip amount.|
| surcharge |    ``` number ```   *example: 2.5*. Surcharge  amount.|
| convenienceFee |    ``` number ```   *example: 2.5*. Amount added for proccessing or handling fees.|   

**ResponseAmountComponents Example:**

```{r}

{
  "subtotal": 8,
  "vatAmount": 0,
  "localTax": 1.3,
  "convenienceFee": 2
}
```  






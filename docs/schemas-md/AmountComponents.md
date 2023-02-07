
# AmountComponents

| *description*:   | *Transaction amounts with multiple components.*|
|----|----|
| subtotal* |    ``` number ```   *example: 8*. Subtotal amount.|
| vatAmount |    ``` number ```   *example: 0*. Value-added tax amount.|
| localTax |    ``` number ```   *example: 1*. Local tax amount.|
| shipping |    ``` number ```   *example: 1.24*. Shipping amount.|
| cashback |    ``` number ```   *example: 2*. Cashback amount.|
| tip |    ``` number ```   *example: 6*. Tip amount.|
| surcharge |    ``` number ```   *example: 2.5*. Surcharge  amount.|  

**AmountComponents Example:**

```{r}

{
  "subtotal": 8,
  "vatAmount": 0,
  "localTax": 1,
  "shipping": 1.24,
  "cashback": 2,
  "tip": 6,
  "surcharge": 2.5
}
```  






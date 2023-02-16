
# AmountComponents

| *description*:   | *Transaction amounts with multiple components.*|
|----|----|
| subtotal* |    ``` number ```  <br/>   *example: 8*.  <br/> Subtotal amount.|
| vatAmount |    ``` number ```  <br/>   *example: 0*.  <br/> Value-added tax amount.|
| localTax |    ``` number ```  <br/>   *example: 1*. <br/>  Local tax amount.|
| shipping |    ``` number ```   <br/>  *example: 1.24*.  <br/> Shipping amount.|
| cashback |    ``` number ```  <br/>   *example: 2*.  <br/> Cashback amount.|
| tip |    ``` number ```   <br/>  *example: 6*. <br/>  Tip amount.|
| surcharge |    ``` number ```   <br/>  *example: 2.5*. <br/>  Surcharge  amount.|  

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







# SepaCredit

| *description*: | *The payment object for SEPA Credit Local Payment.*| 
|----|----|
| iban* |  ``` string ``` <br/> maxLength: 34  <br/> pattern: ^(?!\s*$).+  <br/> *example: DE34500100600032121604*  <br/> Bank account in IBAN format.|
| name* |  ``` string ```   <br/> maxLength: 70  <br/> pattern: ^(?!\s*$).+  <br/> *example: John Doe*  <br/> The name of the Account Holder.|  


**SepaCredit Example:**

```{r}

{
  "iban": "DE34500100600032121604",
  "name": "John Doe"
}
```




  






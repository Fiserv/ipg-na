
# SepaCredit

| *description*: | *The payment object for SEPA Credit Local Payment.*| 
|----|----|
| iban* |  ``` string ```  *maxLength: 34 pattern: ^(?!\s*$).+ example: DE34500100600032121604* Bank account in IBAN format.|
| name* |  ``` string ```  *maxLength: 70 pattern: ^(?!\s*$).+ example: John Doe* The name of the Account Holder.|  


**SepaCredit Example:**

```{r}

{
  "iban": "DE34500100600032121604",
  "name": "John Doe"
}
```




  






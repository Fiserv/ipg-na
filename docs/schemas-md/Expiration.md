
# Expiration

| *description*: | *Required for normal transactions except for payment with 'RECURRING' flags.*| 
|----|----|
| month* |  ``` string ```  *pattern: ^(0[1-9]|1[012])$ example: 03*  Month of the card expiration date in MM format.|
| year* |  ``` string ```  *pattern: ^([0-9]{2})$ example: 21*  Year of the card expiration date in YY format.|  


**Expiration Example:**

```{r}

{
  "month": "03",
  "year": "22"
}
```




  






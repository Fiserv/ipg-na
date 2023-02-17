
# Expiration

| *description*: | *Required for normal transactions except for payment with 'RECURRING' flags.*| 
|----|----|
| month* |  ``` string ```  <br/>  pattern: ^(0[1-9]|1[012])$ <br/> *example: 03*  <br/>  Month of the card expiration date in MM format.|
| year* |  ``` string ```  <br/>  *pattern: ^([0-9]{2})$  <br/> example: 21*  <br/>  Year of the card expiration date in YY format.|  


**Expiration Example:**

```{r}

{
  "month": "03",
  "year": "22"
}
```




  






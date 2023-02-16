
# ConsumerData

| *description*:   | *Consumer data details provided by the payer.*|
|----|----|
| item* |  ConsumerDataItem   <br/> ``` string ```  <br/>  *example: BLIK_CODE*.  <br/> Type of consumer data item. <br/>  Enum:Array [ 1 ] - [ BLIK_CODE ][ BLIK_CODE ]|
| value* |   ``` string ```  <br/> minLength: 1 <br/>  maxLength: 2048 <br/> *example: 1234.*  <br/> Value of consumer data.|

**ConsumerData Example:**

```{r}

{
  "item": "BLIK_CODE",
  "value": "123456"
}
```  






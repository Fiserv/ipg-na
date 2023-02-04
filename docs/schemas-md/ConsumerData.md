
# ConsumerData

| *description*:   | *Consumer data details provided by the payer.*|
|----|----|
| item* |  ConsumerDataItem  ``` string ```  *example: BLIK_CODE*. Type of consumer data item. Enum:Array [ 1 ] - [ BLIK_CODE ][ BLIK_CODE ]|
| value* |   ``` string ```  *minLength: 1 maxLength: 2048 example: 1234.* Value of consumer data.|

**ConsumerData Example:**

```{r}

{
  "item": "BLIK_CODE",
  "value": "123456"
}
```  






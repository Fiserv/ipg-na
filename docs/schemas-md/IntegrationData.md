
# IntegrationData

| *description*:   | *Provides integration data details from the application.*|
|----|----|
| item* |  IntegrationDataItem  <br/>  ``` string ```  <br/>  *example: RETURN_URL*.  <br/> Type of integration data item. <br/>  Enum:Array [ 4 ] - [ FAILURE_RETURN_URL, PAYER_IP, RETURN_URL, USER_AGENT ]|
| value* |   ``` string ```  <br/>  *minLength: 1 <br/>  maxLength: 2048 <br/>  example: "https://clientdomain.com/orderDetails"*  <br/> Value of integration data.|

**IntegrationData Example:**

```{r} 

{
  "item": "RETURN_URL",
  "value": "https://clientdomain.com/orderDetails"
}
```  






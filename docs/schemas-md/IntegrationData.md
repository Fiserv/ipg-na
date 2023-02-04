
# IntegrationData

| *description*:   | *Provides integration data details from the application.*|
|----|----|
| item* |  IntegrationDataItem  ``` string ```  *example: RETURN_URL*. Type of integration data item. Enum:Array [ 4 ] - [ FAILURE_RETURN_URL, PAYER_IP, RETURN_URL, USER_AGENT ]|
| value* |   ``` string ```  *minLength: 1 maxLength: 2048 example: https://clientdomain.com/orderDetails.* Value of integration data.|

**IntegrationData Example:**

```{r}

{
  "item": "RETURN_URL",
  "value": "https://clientdomain.com/orderDetails"
}
```  






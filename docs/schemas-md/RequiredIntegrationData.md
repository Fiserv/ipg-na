
# RequiredIntegrationData

| *description*:   | *Provides details for data requested from the application.*|
|----|----|
| hint |    ``` string ```  <br/>  *maxLength: 2048* <br/>  Description of required integration data that need to be provided.|
| key |  ``` string ```   <br/> *maxLength: 2048* <br/>  Key for required data item.|

**RequiredIntegrationData Example:**

```{r}

{
  "hint": "Payment requires the user agent information on the browser/device.",
  "key": "USER_AGENT"
}
```




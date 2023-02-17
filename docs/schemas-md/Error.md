
# Error

| *description*:   | *Error information.*|
|----|----|
| code |    ``` string ```  <br/>  *example: 2303*.  <br/> Uniquely identifies an error condition. Client applications need to read and handle errors based on this.|
| message |     ``` string ```  <br/>  *example: Invalid credit card number*. <br/>  A generic description of the error condition.|
| details | Detailed information about message format errors.|
|         | **field** :  ``` string ```  <br/>  *example: PaymentCard.number*. <br/>  The property or attribute associated with the error.|
|         | **message** :  ``` string ```  <br/>  *example: may not be null*.  <br/> Information specific to a property or attribute.|
| declineReasonCode |     ``` string ``` <br/>   *example: Do not try again* <br/> Information about the decline reason.|

**Error Example:**

```{r}

{
  "code": "2303",
  "message": "Invalid credit card number"
}   
```




  


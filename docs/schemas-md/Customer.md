
# Customer

| *description*: | *Customer model for customers registered at merchant's website.*|
|----|----|
| id* |    ``` string ```  <br/> *pattern: ^(?!\s*$).+ <br/> *example: 125Xasdf57D* <br/>Unique ID for the customer, if registered. This field is required if the parent object is present.|
| startDate |    ``` string ```   <br/>*example: 2017-01-04* <br/>The timestamp of the customers registration in the merchants platform. Format is YYYY-MM-DD.|
| firstName |    ``` string ```   <br/>*example: John*  <br/>Customer's first name.|
| lastName |    ``` string ```   <br/>*example: Smith* <br/>Customer's last name.|
| middleName |    ``` string ```   <br/> *example: Joseph* <br/>Customer's middle name.|
| email |    ``` string ```   <br/>*example: accept@xyz.com* <br/>Customer's email address.|
| sessionId |    ``` string ```  <br/>*example: session-1* <br/>The unique ID of the current login session. Must be unique for the customer.|
| username |    ``` string ```   <br/>*example: username* <br/>The username of this customer in the merchants system. This field should contain customer-supplied data if available instead of a generated ID. This field can contain the clients email address if it is also used for authentication purposes.|
| gender |    ``` string ```   <br/>*example: male* <br/>The customers gender. Do not set this property if the customer does not specify a gender. <br/>Enum:[ male, female, other ]|
| dateOfBirth |    ``` string ```   <br/>*example: 1982* <br/>The customer's year of birth. Format is YYYY.|
| address | [CustomerAddress](?path=docs/schemas-md/CustomerAddress.md)|
| userDefined |   {<br/> description: A JSON object that can carry any additional information about the customer that might be helpful for fraud detection. <br/> example:  { "previouslyAffected": "Y" }<br/> }|

**Customer Example:**

```{r}

{
  "id": "125Xasdf57D",
  "startDate": "2017-01-04",
  "firstName": "John",
  "lastName": "Smith",
  "middleName": "Joseph",
  "email": "accept@xyz.com",
  "sessionId": "session-1",
  "username": "username",
  "gender": "male",
  "dateOfBirth": "1982",
  "address": {
    "street": "Apartment 123",
    "street2": "123 Main Street",
    "stateProvince": "NY",
    "city": "New York",
    "country": "US",
    "phone": {
      "type": "mobile",
      "number": "212-515-1212"
    },
    "zipPostalCode": "11375"
  },
  "userDefined": {
    "previouslyAffected": "Y"
  }
}
```







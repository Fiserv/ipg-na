
# CarRental

| *description*: | *Additional data specific to the car rental industry.*|
|----|----|
| agreementNumber |    ``` string ```   <br/> maxLength: 20  <br/> *example: 100001145699*  <br/> The car rental agreement number.|
| renterName |    ``` string ```   <br/> maxLength: 20  <br/> *example: Frank Bisignano*  <br/> The name of the person renting the car.|
| returnCity |    ``` string ```  <br/>   maxLength: 20  <br/> *example: Atlanta*  <br/> The city where the rental ends and the car is returned.|
| returnDate |    ``` string ```  <br/>   ($date)  <br/> *example: 2020-10-25*  <br/> The date the car rental ends and the car is returned.|
| pickupDate |    ``` string ```  <br/>   ($date) *example: 2020-10-15* The date the car rental begins.|
| rentalClassId |    ``` string ```   <br/>  maxLength: 6  <br/> *example: ABCDEF*  <br/> The classification of the rental car.|
| extraCharges |  [ExtraCharges](?path=docs/schemas-md/ExtraCharges.md) *[ example: List [ OrderedMap { "chargeItem": "MINI_BAR" }, OrderedMap { "chargeItem": "OTHER" } ]* Information about charges other than rental.| 
| noShowIndicator |    ``` boolean ```   <br/>  *example: false* <br/>  Indicates if the transaction is related to a no-show charge.|

**CarRental Example:**

```{r}

{
  "agreementNumber": "100001145699",
  "renterName": "Frank Bisignano",
  "returnCity": "Atlanta",
  "returnDate": "2020-10-25",
  "pickupDate": "2020-10-15",
  "rentalClassId": "ABCDEF",
  "extraCharges": [
    {
      "chargeItem": "GAS"
    },
    {
      "chargeItem": "EXTRA_MILEAGE"
    }
  ],
  "noShowIndicator": false
}```  







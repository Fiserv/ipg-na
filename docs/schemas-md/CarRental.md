
# CarRental

| *description*: | *Additional data specific to the car rental industry.*|
|----|----|
| agreementNumber |    ``` string ```   *maxLength: 20 example: 100001145699* The car rental agreement number.|
| renterName |    ``` string ```   *maxLength: 20 example: Frank Bisignano* The name of the person renting the car.|
| returnCity |    ``` string ```   *maxLength: 20 example: Atlanta* The city where the rental ends and the car is returned.|
| returnDate |    ``` string ```   *($date) example: 2020-10-25* The date the car rental ends and the car is returned.|
| pickupDate |    ``` string ```   *($date) example: 2020-10-15* The date the car rental begins.|
| rentalClassId |    ``` string ```   *maxLength: 6 example: ABCDEF* The classification of the rental car.|
| extraCharges |  [ExtraCharges](?path=docs/schemas-md/ExtraCharges.md) *[ example: List [ OrderedMap { "chargeItem": "MINI_BAR" }, OrderedMap { "chargeItem": "OTHER" } ]* Information about charges other than rental.| 
| noShowIndicator |    ``` boolean ```   *example: false* Indicates if the transaction is related to a no-show charge.|

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







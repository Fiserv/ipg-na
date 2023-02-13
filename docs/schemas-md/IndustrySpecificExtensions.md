
# IndustrySpecificExtensions

| *description*:   | *Industry-specific information.*|
|----|----|
| airline | [Airline](?path=docs/schemas-md/Airline.md)| 
| lodging | [Lodging](?path=docs/schemas-md/Lodging.md)|
| carRental | [CarRental](?path=docs/schemas-md/CarRental.md)|
| mcc6012 | [Mcc6012](?path=docs/schemas-md/Mcc6012.md)|


**IndustrySpecificExtensions Example:**

```{r}

{
  "airline": {
    "passengerName": "John Doe",
    "ticketNumber": "PCLAN123",
    "carrierName": "Quatar Airline",
    "reservationSystem": "START",
    "travelRoute": [
      {
        "departureDate": "2018-10-15",
        "origin": "ATL",
        "destination": "DOH"
      }
    ]
  },
  "lodging": {
    "arrivalDate": "2010-05-15",
    "departureDate": "2018-01-28",
    "folioNumber": "12200054891",
    "extraCharges": [
      {
        "chargeItem": "MINI_BAR"
      },
      {
        "chargeItem": "OTHER"
      }
    ],
    "noShowIndicator": false
  },
  "carRental": {
    "agreementNumber": "AGR 123",
    "renterName": "John Doe",
    "returnCity": "ATL",
    "returnDare": "2018-10-25",
    "pickupDate": "2018-10-15"
  },
  "mcc6012": {
    "dateOfBirth": "20200505",
    "accountFirst6": "411111",
    "accountLast4": "2343",
    "accountNum": "546789900034567",
    "postCode": "30101",
    "surname": "Walker"
  }
}
```






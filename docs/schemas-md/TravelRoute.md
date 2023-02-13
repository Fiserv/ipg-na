
# TravelRoute

| *description*: | *Additional information about the route.*|
|----|----|
| departureDate |    ``` string ```   *($date) example: 2018-	01-28 Date of departure.|
| origin |    ``` string ```   *maxLength: 3 example: MIA* The IATA code for the departure airport.|
| destination |    ``` string ```   *maxLength: 3 example: ATL* The IATA code for the destination. airport.|
| carrierCode |    ``` string ```   *maxLength: 2 example: DL* The IATA code for the carrier.|
| serviceClass |    ``` string ```   *maxLength: 1 example: J* The airline code for the service class of the ticket.|
| stopoverType |    ``` string ```   *example: DIRECT* Indicates whether the route is direct. Enum:[ DIRECT, STOPOVER ]|
| fareBasisCode |    ``` string ```   *maxLength: 2 example: F* The airline fare basis code.|
| departureTax |    ``` number ```   *maximum: 999999999999 example: 75* Fee charged by a country when a person leaves the country.|
| flightNumber |    ``` string ```   *maxLength: 10 example: 765599* The airline flight number associated with the ticket.|


**TravelRoute Example:**

```{r}

{
      "departureDate": "2018-01-28",
      "origin": "MIA",
      "destination": "ATL",
      "carrierCode": "DL",
      "serviceClass": "J",
      "stopoverType": "DIRECT",
      "fareBasisCode": "F",
      "departureTax": 75,
      "flightNumber": "765599"
}
```  







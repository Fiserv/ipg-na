
# TravelRoute

| *description*: | *Additional information about the route.*|
|----|----|
| departureDate |    ``` string ```  <br/>   *($date) example: 2018-01-28 <br/>  Date of departure.|
| origin |    ``` string ```   <br/>  *maxLength: 3  <br/> example: MIA*  <br/> The IATA code for the departure airport.|
| destination |    ``` string ```    <br/> *maxLength: 3 <br/> example: ATL* <br/> The IATA code for the destination. airport.|
| carrierCode |    ``` string ```   <br/>  *maxLength: 2  <br/> example: DL*  <br/> The IATA code for the carrier.|
| serviceClass |    ``` string ```    <br/> *maxLength: 1  <br/> example: J*  <br/> The airline code for the service class of the ticket.|
| stopoverType |    ``` string ```    <br/> *example: DIRECT*  <br/> Indicates whether the route is direct.  <br/> Enum:[ DIRECT, STOPOVER ]|
| fareBasisCode |    ``` string ```   <br/>  *maxLength: 2  <br/> example: F* <br/>  The airline fare basis code.|
| departureTax |    ``` number ```   <br/>  *maximum: 999999999999  <br/> example: 75*  <br/> Fee charged by a country when a person leaves the country.|
| flightNumber |    ``` string ```    <br/> *maxLength: 10  <br/> example: 765599*  <br/> The airline flight number associated with the ticket.|


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







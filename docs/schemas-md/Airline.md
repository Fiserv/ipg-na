
# Airline

| *description*:   | *Additional data specific to the airline industry.*|
|----|----|
| passengerName |   ``` string ```   <br/> maxLength: 30  <br/> *example: Jeff Yabuki*  <br/> The passenger name associated with the transaction.|
| ticketNumber |   ``` string ```   <br/> maxLength: 20 <br/> *example: 52300448*  <br/> The airline ticket number associated with the transaction.|
| issuingCarrier |  ``` string ```   <br/> maxLength: 20 <br/> *example: Frontier Airlines* <br/>  The carrier that issued the ticket.|
| carrierName |  ``` string ```   <br/> maxLength: 20 <br/> *example: Delta Air Lines*  <br/> The carrier associated with the transaction.|
| travelAgencyIataCode | 	 ``` string ```   <br/> maxLength: 20 <br/> *example: 10584410* <br/>  The IATA code associated with the travel agency.|
| travelAgencyName | 	 ``` string ```   <br/> maxLength: 30 <br/> *example: A Travis Gent LLC*  <br/> The business name of the travel agency.|
| airlinePlanNumber | 	 ``` string ```   <br/> maxLength: 2 <br/> *example: 11*  <br/> The airline plan number associated with the transaction.|
| airlineInvoiceNumber | 	 ``` string ```   <br/> maxLength: 6 <br/> *example: 664422* <br/> The invoice number used by the airline.|
| reservationSystem | 	 ``` string ```   <br/> *example: DELTA*  <br/> The reservation system used to create the ticket.  <br/> Enum:[ START, TWA, DELTA, SABRE, COVIA_APOLLO, DR_BLANK, DER, TUI ]|
| restricted | 	 ``` boolean ```   <br/> *example: true*  <br/> If the transaction is associated with a restricted class fare.|
| travelRoute |  [TravelRoute](?path=docs/schemas-md/TravelRoute.md) , <br/>  maxItems: 4  <br/> *example: List [ OrderedMap { "departureDate": "2018-01-28", "origin": "MIA", "destination": "ATL", "carrierCode": "DL", "serviceClass": "J", "stopoverType": "DIRECT", "fareBasisCode": "F", "departureTax": 75, "flightNumber": "765599" } ]*  -   <br/> Array containing up to 4 items that describe the route associated with the transaction.|
| relatedTicketNumber |  ``` string ```   <br/> maxLength: 20 <br/> *example: 11223344556* The number of any other tickets associated with the transaction ticket.|
| ancillaryServiceCategory |  [AncillaryServiceCategory](?path=docs/schemas-md/AncillaryServiceCategory.md) ,  <br/> *example: List [ OrderedMap { "serviceCategory": "BAGGAGE_FEE" }, OrderedMap { "serviceCategory": "CARBON_OFFSET" } ]*  -  <br/>  Identify the purchase of ancillary goods or services with a false value. If this element is not provided, the transaction is assumed to be a purchase of an airline ticket.|
| ticketPurchase |  ``` boolean ```   <br/> *example: true*  <br/> Identifies if the transaction is a ticket purchase.|

**Airline Example:**

```{r}

{
  "passengerName": "Jeff Yabuki",
  "ticketNumber": "52300448",
  "issuingCarrier": "Frontier Airlines",
  "carrierName": "Delta Air Lines",
  "travelAgencyIataCode": "10584410",
  "travelAgencyName": "A Travis Gent LLC",
  "airlinePlanNumber": "11",
  "airlineInvoiceNumber": "664422",
  "reservationSystem": "DELTA",
  "restricted": true,
  "travelRoute": [
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
  ],
  "relatedTicketNumber": "11223344556",
  "ancillaryServiceCategory": [
    {
      "serviceCategory": "BAGGAGE_FEE"
    },
    {
      "serviceCategory": "CARBON_OFFSET"
    }
  ],
  "ticketPurchase": true
}
```





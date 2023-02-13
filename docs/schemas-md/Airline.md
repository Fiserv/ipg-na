
# Airline

| *description*:   | *Additional data specific to the airline industry.*|
|----|----|
| passengerName |   ``` string ```   *maxLength: 30 example: Jeff Yabuki* The passenger name associated with the transaction.|
| ticketNumber |   ``` string ```   *maxLength: 20 example: 52300448* The airline ticket number associated with the transaction.|
| issuingCarrier |  ``` string ```   *maxLength: 20 example: Frontier Airlines* The carrier that issued the ticket.|
| carrierName |  ``` string ```   *maxLength: 20 example: Delta Air Lines* The carrier associated with the transaction.|
| travelAgencyIataCode | 	 ``` string ```   *maxLength: 20 example: 10584410* The IATA code associated with the travel agency.|
| travelAgencyName | 	 ``` string ```   *maxLength: 30 example: A Travis Gent LLC* The business name of the travel agency.|
| airlinePlanNumber | 	 ``` string ```   *maxLength: 2 example: 11* The airline plan number associated with the transaction.|
| airlineInvoiceNumber | 	 ``` string ```   *maxLength: 6 example: 664422* The invoice number used by the airline.|
| reservationSystem | 	 ``` string ```   *example: DELTA* The reservation system used to create the ticket. Enum:[ START, TWA, DELTA, SABRE, COVIA_APOLLO, DR_BLANK, DER, TUI ]|
| restricted | 	 ``` boolean ```   *example: true* If the transaction is associated with a restricted class fare.|
| travelRoute |  [TravelRoute](?path=docs/schemas-md/TravelRoute.md) , maxItems: 4 *example: List [ OrderedMap { "departureDate": "2018-01-28", "origin": "MIA", "destination": "ATL", "carrierCode": "DL", "serviceClass": "J", "stopoverType": "DIRECT", "fareBasisCode": "F", "departureTax": 75, "flightNumber": "765599" } ]*  -  Array containing up to 4 items that describe the route associated with the transaction.|
| relatedTicketNumber |  ``` string ```   *maxLength: 20 example: 11223344556* The number of any other tickets associated with the transaction ticket.|
| ancillaryServiceCategory |  [AncillaryServiceCategory](?path=docs/schemas-md/AncillaryServiceCategory.md) , *example: List [ OrderedMap { "serviceCategory": "BAGGAGE_FEE" }, OrderedMap { "serviceCategory": "CARBON_OFFSET" } ]*  -  Identify the purchase of ancillary goods or services with a false value. If this element is not provided, the transaction is assumed to be a purchase of an airline ticket.|
| ticketPurchase |  ``` boolean ```   *example: true* Identifies if the transaction is a ticket purchase.|

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





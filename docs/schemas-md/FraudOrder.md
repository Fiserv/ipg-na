
# FraudOrder

| *description*: | *The list of items included in the order.*|
|----|----|
| shipToAddress | [ShipToAddress](?path=docs/schemas-md/ShipToAddress.md)|
| items |  [ <br/> example: List [ OrderedMap { "id": "PRODCODE1", "name": "The Art of Computer Programming", "quantity": "litre", "unit": "1", "unitPrice": "{\"value\": 7300, \"currency\": \"USD\"}", "categories": List [ List [ "Books", "Computers & Technology", "Programming" ], List [ "Books", "Text Books", "Computer Science" ] ], "detailsUrl": "https://mystore.domain/product/PRODCODE1", "userDefined": OrderedMap { "weight": 5021.23, "vat": 0.06 } } ] <br/> The list of items included in the order. <br/>	[FraudOrderItems](?path=docs/schemas-md/FraudOrderItems.md)]|
| userDefined |   {<br/> description: A JSON object that can carry any additional information about the customer that might be helpful for fraud detection. <br/> example:  { "highFraudVolume": true }<br/> }|

**FraudOrder Example:**

```{r}

{
  "shipToAddress": {
    "phone": "404-404-4040",
    "address1": "5565 Glenridge Connector",
    "city": "Atlanta",
    "state": "GA",
    "zip": "30342",
    "country": "US"
  },
  "items": [
    {
      "id": "PRODCODE1",
      "name": "The Art of Computer Programming",
      "quantity": "litre",
      "unit": "10.23",
      "unitPrice": "{\"value\": 7300, \"currency\": \"USD\"}",
      "categories": [
        [
          "Books",
          "Computers & Technology",
          "Programming"
        ],
        [
          "Books",
          "Text Books",
          "Computer Science"
        ]
      ],
      "detailsUrl": "https://mystore.domain/product/PRODCODE1",
      "userDefined": {
        "weight": 5021.23,
        "vat": 0.06
      }
    }
  ],
  "userDefined": {
    "delivery": "express",
    "carrier": "ups"
  }
}
```








# FraudOrderItems

| *description*: | *Product details.*|
|----|----|
| id |    ``` string ```   <br/>*example: PRODCODE1* <br/> A unique ID associated with the product. Must be unique within the merchant's system.|
| name |    ``` string ```   <br/>*example: The Art of Computer Programming* <br/> A name or short description of the product.|
| quantity |    ``` string ```   <br/>  *example: litre* <br/> The unit in which the product is sold (e.g. litre, kilogram, etc). Leave empty if the product is sold as a complete unit.|
| unit |    ``` string ```   <br/> *example: 1* <br/> The number of units sold. Set to 1 if there is only one unit of the item. Leave empty if the quantity is unknown at the time of the request.|
| unitPrice | ``` string ```  <br/> *example: {"value": 7300, "currency": "USD"}* <br/> The price per unit.|
| categories | [ <br/> example: List [ List [ "Books, Computers & Technology, Programming" ], List [ "Books, Text Books, Computer Science" ] ] <br/> The categories that this product belongs to. <br/> [ <br/> example: List [ "Books, Programming" ] <br/> string <br/> 	example: Books] <br/> ] <br/> ] | 
| detailsUrl | ``` string ```  <br/> *example: https://mystore.domain/product/PRODCODE1* <br/> The URL to the merchant's management system, for reporting and analysis.|
| userDefined |   {<br/> description: A JSON object that can carry any additional information about the customer that might be helpful for fraud detection. <br/> example:  { "phoneBrand": "samsung" }<br/> }|

**FraudOrderItems Example:**

```{r}

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
```






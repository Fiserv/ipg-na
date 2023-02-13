
# BasketItem

| *description*:   | *Item details.*|
|----|----|
| id |    ``` string ```  A unique ID associated with the product.|
| description |    ``` string ```  *example: The Art of Computer Programming*  A name or short description of the product.|
| subTotal |    ``` number ```  *example: 8* Subtotal amount.|
| valueAddedTax |    ``` number ``` *example: 0* Value added tax amount.|
| localTax |    ``` number ``` *example: 1* Local tax amount.|
| deliveryAmount |    ``` number ``` *example: 1* Delivery amount.|
| chargeTotal |    ``` number ``` *example: 1* Charge Total amount.|
| currency |    ``` string ``` *pattern: ([A-Z]{3})|([0-9]{3}) example: USD* The currency of the original transaction.|
| quantity |    ``` number ``` *example: 1* The unit in which the product is sold (e.g. litre, kilogram, etc). Leave empty if the product is sold as a complete unit.|
| unitPrice |    ``` number ``` *example: 1.719* The unit price is number with 3 decimal precision.|
| category |    ``` string ```  Category of the product.|
| detailedCategory |    Detailed Category of the product.|
| options  | [ Option details [Option](?path=docs/schemas-md/Option.md)] |  









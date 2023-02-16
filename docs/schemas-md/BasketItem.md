
# BasketItem

| *description*:   | *Item details.*|
|----|----|
| id |    ``` string ```  <br/>  A unique ID associated with the product.|
| description |    ``` string ```  <br/>  *example: The Art of Computer Programming*  <br/>  A name or short description of the product.|
| subTotal |    ``` number ``` <br/>   *example: 8*  <br/> Subtotal amount.|
| valueAddedTax |    ``` number ``` <br/>  *example: 0* <br/>  Value added tax amount.|
| localTax |    ``` number ``` <br/>  *example: 1*  <br/> Local tax amount.|
| deliveryAmount |    ``` number ``` <br/>  *example: 1* <br/>  Delivery amount.|
| chargeTotal |    ``` number ```  <br/> *example: 1*  <br/> Charge Total amount.|
| currency |    ``` string ```  <br/> pattern: ([A-Z]{3})|([0-9]{3})  <br/> *example: USD*  <br/> The currency of the original transaction.|
| quantity |    ``` number ```  <br/> *example: 1*  <br/> The unit in which the product is sold (e.g. litre, kilogram, etc). Leave empty if the product is sold as a complete unit.|
| unitPrice |    ``` number ```  <br/> *example: 1.719*  <br/> The unit price is number with 3 decimal precision.|
| category |    ``` string ```   <br/> Category of the product.|
| detailedCategory |    Detailed Category of the product.|
| options  | [ Option details [Option](?path=docs/schemas-md/Option.md)] |  









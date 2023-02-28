
# PaymentFacilitator

| *description*:   | *Payment facilitator details provided by the merchant.*|
|----|----|
| externalMerchantId |    ``` string ```  <br/>  *pattern: ^(?!\s*$).+ example: 151623999* <br/>  External merchant ID of the payment facilitator.|
| paymentFacilitatorId |    ``` string ```  <br/>  *pattern: \d{1,11}  <br/> example: 13579246801*  <br/> Independent sales organization (ISO) ID provided by Mastercard.|
| saleOrganizationId |   ``` string ```  <br/>  *example: Unauthenticated* <br/> The type of the response.  <br/> Enum:    > Array [ 9 ] - [ BadRequest, Unauthenticated, Unauthorized, NotFound, GatewayDeclined, EndpointDeclined, ServerError, EndpointCommunicationError, UnsupportedMediaType ]|
| name |  ``` string ```  <br/> maxLength: 50  <br/> pattern: ^(?!\s*$).+ <br/> example: First Reseller*  <br/> Payment facilitator name.|
| subMerchantData |  [SubMerchantData](?path=docs/schemas-md/SubMerchantData.md)|        

**PaymentFacilitator Example:**

```{r}

{
  "externalMerchantId": "12345",
  "paymentFacilitatorId": "123123123",
  "saleOrganizationId": "123124214",
  "name": "First Reseller",
  "subMerchantData": {
    "mcc": "1432",
    "legalName": "First Merchant",
    "timezone": "Europe/London",
    "address": {
      "address1": "123 Main St.",
      "city": "Sandy Springs",
      "region": "Georgia",
      "postalCode": "30303",
      "country": "USA"
    },
    "document": {
      "type": "NATIONAL_IDENTITY",
      "number": "12345666544"
    },
    "merchantId": "12435325235"
  }
}
``` 

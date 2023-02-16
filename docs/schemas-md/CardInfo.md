
# CardInfo

| *description*:   | *Card information.*|
|----|----|
| brand |    ``` string ``` <br/> *example: VISA* <br/>  The card brand.|
| brandProductId |    ``` string ```  <br/>  *example: VISA BUSINESS*  <br/> The product ID of the brand.|
| cardFunction | [CardFunction](?path=docs/schemas-md/CardFunction.md)|
| commercialCard |    ``` string ``` <br/>   *example: CORPORATE*  <br/> Indicates whether it is a corporate or non-corporate card. <br/>  Enum:[ CORPORATE, NON_CORPORATE ]|
| issuerCountry |    ``` string ``` <br/>   *example: DE* <br/>  The country of the issuer.|
| issuerName |    ``` string ```  <br/>  *example: First National Bank of Omaha*  <br/> The name of the issuer.|

**CardInfo Example:**

```{r}

{
  "brand": "VISA",
  "brandProductId": "VISA BUSINESS",
  "cardFunction": "CREDIT",
  "commercialCard": "CORPORATE",
  "issuerCountry": "DE",
  "issuerName": "First National Bank of Omaha"
}
```  
  


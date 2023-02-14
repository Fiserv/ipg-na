
# CardInfo

| *description*:   | *Card information.*|
|----|----|
| brand |    ``` string ```  *example: VISA* The card brand.|
| brandProductId |    ``` string ```  *example: VISA BUSINESS* The product ID of the brand.|
| cardFunction | [CardFunction](?path=docs/schemas-md/CardFunction.md)|
| commercialCard |    ``` string ```  *example: CORPORATE* Indicates whether it is a corporate or non-corporate card.- Enum:[ CORPORATE, NON_CORPORATE ]|
| issuerCountry |    ``` string ```  *example: DE* The country of the issuer.|
| issuerName |    ``` string ```  *example: First National Bank of Omaha* The name of the issuer.|

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
  


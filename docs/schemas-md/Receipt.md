
# Receipt

| *description*: | *Provides POS receipt data.*|
|----|----|
| type* |    ``` string ```  <br/>  *example: merchant*  <br/> Defines the consumer of the receipt (e.g. cardholder, merchant). Enum:[ cardholder, merchant ]|
| data | [  example: List [ OrderedMap { "endOfLine": true, "text": " MerchantName " }, OrderedMap { "endOfLine": true, "text": "--------------------------------" } ].  Array of formatted lines that represents the actual receipt data, that can be printed out. [ReceiptLine](?path=docs/schemas-md/ReceiptLine.md)|

**Receipt Example:**

```{r}

{
  "type": "cardholder",
  "data": [
    {
      "endOfLine": true,
      "text": "        Example Merchant        "
    },
    {
      "endOfLine": true,
      "text": "--------------------------------"
    },
    {
      "endOfLine": true,
      "text": "       Amount: 45.00 EURO       "
    }
  ]
}
```  







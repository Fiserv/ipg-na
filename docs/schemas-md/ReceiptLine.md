
# ReceiptLine

| *description*: | *Represents a line in the receipt response.*|
|----|----|
| endOfLine |    ``` boolean ```  <br/> *example: true*  <br/> Flag to indicate if the text ends at the end of this receipt line.|
| text |``` string ```  <br/> *example:MerchantName*  <br/> Text that represents a line of the actual receipt data, that can be printed out.|

**ReceiptLine Example:**

```{r}

{
  "endOfLine": true,
  "text": "--------------------------------"
}
```  








# AdditionalTransactionDetails

| *description*:   | *Additional transaction details for transaction response.*|
|----|----|
| comments |    ``` string ```  *maxLength: 1024   example: This is a comment.*  Comments for the payment.|
| invoiceNumber | ``` string ```  *maxLength: 48   example: 551294633441*  Invoice number.|
| purchaseOrderNumber | ``` string ```  *maxLength: 128   example: 1223456*  Purchase order number.|  
| disbursementTransType | ``` string ```  *example: FUNDING*  The type of debit disbursement transaction. Enum:Array [ 2 ] - Enum:Array [ 2 ] |
| walletProvider | ``` string ```  *example: APPLE_PAY*  The wallet provider type. Enum:Array [ 4 ] - [ GOOGLE_PAY, APPLE_PAY, SAMSUNG_PAY, MASTERPASS ]| 
| receipts | *minItems: 1 maxItems: 2 example: List [ OrderedMap { "type": "cardholder", "locale": "de-DE" }, OrderedMap { "type": "merchant", "locale": "en", "linewidth": 48 } ]*  Provides request information that is necessary to generate receipts. [ReceiptRequestInfo](?path=docs/schemas-md/ReceiptRequestInfo.md)|
| additionalResponseData | [AdditionalResponseData](?path=docs/schemas-md/AdditionalResponseData.md)|  

**AdditionalTransactionDetails Example:**

```{r}

{
  "comments": "This is a comment",
  "invoiceNumber": "551294633441",
  "purchaseOrderNumber": "1223456"
}
```  




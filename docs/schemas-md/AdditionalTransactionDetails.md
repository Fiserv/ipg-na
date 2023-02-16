
# AdditionalTransactionDetails

| *description*:   | *Additional transaction details for transaction response.*|
|----|----|
| comments |    ``` string ```  <br/>  *maxLength: 1024   example: This is a comment.*  <br/>  Comments for the payment.|
| invoiceNumber | ``` string ```  <br/>  *maxLength: 48   example: 551294633441*  <br/>  Invoice number.|
| purchaseOrderNumber | ``` string ```  <br/>  maxLength: 128   <br/>  *example: 1223456*  <br/>  Purchase order number.|  
| disbursementTransType | ``` string ```  <br/>  *example: FUNDING*   <br/> The type of debit disbursement transaction. <br/>  Enum:Array [ 2 ] - Enum:Array [ 2 ] |
| walletProvider | ``` string ```  <br/>  *example: APPLE_PAY*  <br/>  The wallet provider type.  <br/> Enum:Array [ 4 ] - [ GOOGLE_PAY, APPLE_PAY, SAMSUNG_PAY, MASTERPASS ]| 
| receipts | minItems: 1 maxItems: 2 <br/>  *example: List [ OrderedMap { "type": "cardholder", "locale": "de-DE" }, OrderedMap { "type": "merchant", "locale": "en", "linewidth": 48 } ]*  <br/>  Provides request information that is necessary to generate receipts. [ReceiptRequestInfo](?path=docs/schemas-md/ReceiptRequestInfo.md)|
| additionalResponseData | [AdditionalResponseData](?path=docs/schemas-md/AdditionalResponseData.md)|  

**AdditionalTransactionDetails Example:**

```{r}

{
  "comments": "This is a comment",
  "invoiceNumber": "551294633441",
  "purchaseOrderNumber": "1223456"
}
```  




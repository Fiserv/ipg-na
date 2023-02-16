
# AdditionalDetails

| *description*:   | *Merchant supplied tracking numbers.*|
|----|----|
| comments |    ``` string ```  <br/>  maxLength: 1024    <br/> *example: This is a comment.*  <br/>  Comments for the payment.|
| invoiceNumber | ``` string ```   <br/> maxLength: 48   <br/>  *example: 551294633441*  <br/>  Invoice number.|
| invoicePeriod | ``` string ```  *maxLength: 25 pattern: ^(?!\s*$).+   example: Alpharetta*  Sender city.|  
| purchaseOrderNumber | ``` string ```   <br/> maxLength: 128   <br/>  *example: 1223456*   <br/> Purchase order number.|  
| mrchntRefData | ``` string ```   <br/> maxLength: 30    <br/> *example: 1223456*  <br/>  Merchant Reference Data 2.| 
| operatorId | ``` string ```   <br/> maxLength: 35  <br/> pattern: ^\S$|^\S.*\S$  <br/>   The operator ID.| 
| salesSystemId | ``` string ```  <br/> maxLength: 50  <br/> pattern:^\S$|^\S.*\S$  <br/>  The sales system ID.|  
| ipgDeferredAuth | ``` boolean ```  <br/>  *example: true*  <br/> Indicates if the particular transaction is a deferred authorization.|   
| highRiskPurchaseIndicator* |  ``` boolean ```   <br/> *example: true*   <br/> this is highRiskPurchaseIndicator.|
| receipts | minItems: 1  <br/> maxItems: 2  <br/> *example: List [ OrderedMap { "type": "cardholder", "locale": "de-DE" }, OrderedMap { "type": "merchant", "locale": "en", "linewidth": 48 } ]*  <br/> Provides request information that is necessary to generate receipts.  <br/> [ReceiptRequestInfo](?path=docs/schemas-md/ReceiptRequestInfo.md)|  
| scaExemptionType | ``` string ```  <br/>  *example: TRA Exemption*  <br/> Strong customer authentication exemption type indicator. <br/>  Enum:Array [ 6 ] <br/>  [ Low Value Exemption, TRA Exemption, Trusted Merchant Exemption, SCP Exemption, Delegated Authentication, Authentication Outage Exception ]|
| scaVisaMerchantID | ``` string ```   <br/> maxLength: 8  <br/> *example: 12312311*  <br/> Eight-character Visa merchant identifier (VMID) assigned by Visa, required for trusted merchant and delegated authentication.|
| businessApplicationIdentifier | ``` string ```   <br/> *example: ACCOUNT_TO_ACCOUNT* <br/>  Indicates the indended use of the Account Funding Transaction. For Visa Only.  <br/> Enum:Array [ 20 ] - [ ACCOUNT_TO_ACCOUNT, BANK_INITIATED_TRANSFER, BUSINESS_TO_BUSINESS, CARD_BILL_PAYMENT, FUNDS_DISBURSEMENT, FUND_TRANSFER, GAMBLING_PAYOUT, GENERAL_FUNDS_DISBURSEMENT, GOVERNMENT_DISBURSEMENT, LOYALTY_PAYMENTS, MERCHANT_DISBURSEMENT, MERCHANT_PAYMENT, NON_CARD_BILL_PAYMENT, ONLINE_GAMBLING_PAYOUT, PAYROLL_OR_PENSION_DISBURSEMENT, PERSON_TO_PERSON, TOPUP_FOR_ENHANCED_PREPAID_LOADS, TOP_OFF, WALLET_TRANSFER, ZERO_DOLLAR_AUTHORIZATION ]|
| transactionTypeIdentifier | ``` string ```  <br/>  *example: BUSINESS_DISBURSEMENT_MONEY_SEND*  <br/> Indicates the indended use of the Account Funding Transaction. For Mastercard Only. <br/>  Enum:Array [ 15 ] - [ BUSINESS_DISBURSEMENT_MONEY_SEND, BUSINESS_DISBURSEMENT_MONEY_TRANSFER, BUSINESS_TO_BUSINESS_MONEY_SEND, BUSINESS_TO_BUSINESS_MONEY_TRANSFER, CARD_BILL_PAYMENT_MONEY_SEND, CARD_BILL_PAYMENT_MONEY_TRANSFER, GOVERNMENT_DISBURSEMENT_NONPROFIT, OWN_ACCOUNT_MONEY_SEND, OWN_ACCOUNT_MONEY_TRANSFER, OWN_DEBIT_PREPAID_TRANSFER, OWN_WALLET_TRANSFER, PERSON_TO_PERSON_CARD_ACCOUNT, PERSON_TO_PERSON_MONEY_SEND, PERSON_TO_PERSON_MONEY_TRANSFER, RAPID_MERCHANT_SETTLEMENT ]|  


**AdditionalDetails Example:**

```{r}

{
  "comments": "This is a comment",
  "invoiceNumber": "551294633441",
  "invoicePeriod": "12/19",
  "purchaseOrderNumber": "1223456",
  "operatorId": "OPERATOR_ID_123XXX",
  "salesSystemId": "W-EU-H3866-FLS2",
  "ipgDeferredAuth": true,
  "allowPartialApproval": true,
  "highRiskPurchaseIndicator": true,
  "receipts": [
    {
      "type": "cardholder",
      "locale": "fr"
    }
  ],
  "scaExemptionType": "Low Value Exemption",
  "scaVisaMerchantID": "12312311",
  "businessApplicationIdentifier": "ACCOUNT_TO_ACCOUNT",
  "transactionTypeIdentifier": "BUSINESS_DISBURSEMENT_MONEY_SEND"
}
```




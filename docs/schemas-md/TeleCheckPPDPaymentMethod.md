
# TeleCheckPPDPaymentMethod

| *description*: | *ACH TeleCheck payment method for Prearranged Payments and Deposits application type.*|
|----|----|
| achType* |    ``` string ```  <br/> *example: TeleCheckICAPaymentMethod*  <br/>  ACH application type values will be one of either TeleCheckICAPaymentMethod or TeleCheckCBPPaymentMethod or TeleCheckPPDPaymentMethod.|
| routingNumber* | ``` string ```  <br/>  *minLength: 9  <br/> maxLength: 9  <br/> pattern: ^[0-9]+$  <br/> example: 128367331*  <br/> Bank routing number.|
| accountNumber* | ``` string ```  <br/>  *minLength: 1 <br/>  maxLength: 56 <br/>  pattern: ^[0-9]+$  <br/> example: 2398649823984789&*  <br/> Bank account number.|
| accountType* | ``` string ```  <br/>  *example: C*  <br/> Identifies if the account type is checking or savings. <br/>  Enum:[ C, S ]|
| checkNumber | ``` string ```  *maxLength: 10 pattern: ^[0-9]+$ example: 9878867880* Check number.|
| checkType* | ``` string ```  <br/>  *example: P*  <br/> Identifies if the check type is personal or company.  <br/> Enum:[ P, C ]|
| productCode | ``` string ```   <br/> *maxLength: 6  <br/> pattern: ^[0-9]+$  <br/> example: 128367*  <br/> Identifies the product code in the transaction.|
| manualIdInfo | [IdInfo](?path=docs/schemas-md/IdInfo.md)|
| supplementIdInfo | [IdInfo](?path=docs/schemas-md/IdInfo.md)|
| agentId | ``` string ```   <br/> *maxLength: 6  <br/> pattern: (?=.*[^\s])^[^|]+$  <br/> example: RVK001*  <br/> Used to track the agent transaction activity.|
| terminalId | ``` string ```   <br/> *maxLength: 10  <br/> pattern: ^[0-9]+$ <br/>  example: 1283673312* Identifies the register or lane number where the original sale transaction occurred.|
| registrationId | ``` string ```   <br/> *maxLength: 50  <br/> pattern: (?=.*[^\s])^[^|]+$  <br/> example: 12345*  <br/> Unique ID assigned by the merchant for the consumer (never recycled). It is an additional level of authentication. To use this feature, the merchant must work with TeleCheck Risk to discuss. Registration IDs must not be generated for an existing or returning consumer returns. The single registration ID must be unique per consumer.|
| registrationDate | ``` string ```  <br/>  *($date)  <br/> example: 2019-10-02*  <br/> Date the consumer originally registered in format MMDDYYYY.|
| releaseType | ``` string ```   <br/> *example: P*  <br/> Release type is used as a risk variable to gauge risk level when the merchant is releasing the purchased merchandise. <br/>  Enum:[ C, D, P, T ]|
| vipCustomer | ``` string ```  <br/>  *example: Y*  <br/> Flags a transaction as a VIP order (based on merchant criteria). This field should not be sent for non-VIP orders.  <br/> Enum:[ Y, N ]|
| sessionId* | ``` string ```  *maxLength: 128 pattern: (?=.*[^\s])^[^|]+$ example: fb2e77d.47a0479900504cb3ab4a1f626d174d2d* Session identifier.|
| terminalState | ``` string ```   <br/> *maxLength: 2  <br/> pattern: ^[A-Z]{2}$  <br/> example: GA*  <br/> Identifies the US state or territory where the original sale transaction occurred.|
| terminalCity | ``` string ```  <br/>  *maxLength: 16  <br/> pattern: (?=.*[^\s])^[^|]+$  <br/> example: Atlanta*  <br/> Identifies the city where the original sale transaction occurred.|
| achBillTo |{ [achBillTo](?path=docs/schemas-md/AchBillTo.md) }|  
| recurringType | [AchRecurringType](?path=docs/schemas-md/AchRecurringType.md)|  


**TeleCheckPPDPaymentMethod Example:**

```{r}

{
  "achType": "TeleCheckPPDPaymentMethod",
  "routingNumber": "128367331",
  "accountNumber": "2398649823984789",
  "accountType": "S",
  "checkNumber": "9878867880",
  "checkType": "P",
  "productCode": "12836",
  "manualIdInfo": {
    "idType": "DL",
    "idData": "12345678"
  },
  "agentId": "RVK001",
  "terminalId": "1283673312",
  "registrationId": "12345",
  "releaseType": "P",
  "vipCustomer": "Y",
  "sessionId": "fb2e77d.47a0479900504cb3ab4a1f626d174d2d",
  "terminalState": "GA",
  "terminalCity": "Atlanta",
  "recurringType": "Single"
}
```





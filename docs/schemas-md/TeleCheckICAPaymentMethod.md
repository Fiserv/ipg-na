
# TeleCheckICAPaymentMethod

| *description*: | *ACH TeleCheck payment method for internet check acceptance application type.*|
|----|----|
| achType* |    ``` string ```   *example: TeleCheckICAPaymentMethod* ACH application type values will be one of either TeleCheckICAPaymentMethod or TeleCheckCBPPaymentMethod or TeleCheckPPDPaymentMethod.|
| routingNumber* | ``` string ```  *minLength: 9 maxLength: 9 pattern: ^[0-9]+$ example: 128367331* Bank routing number.|
| accountNumber* | ``` string ```  *minLength: 1 maxLength: 56 pattern: ^[0-9]+$ example: 2398649823984789&* Bank account number.|
| accountType* | ``` string ```  *example: C* Identifies if the account type is checking or savings. Enum:[ C, S ]|
| checkNumber | ``` string ```  *maxLength: 10 pattern: ^[0-9]+$ example: 9878867880* Check number.|
| checkType* | ``` string ```  *example: P* Identifies if the check type is personal or company. Enum:[ P, C ]|
| productCode | ``` string ```  *maxLength: 6 pattern: ^[0-9]+$ example: 128367* Identifies the product code in the transaction.|
| manualIdInfo | [IdInfo](?path=docs/schemas-md/IdInfo.md)|
| supplementIdInfo | [IdInfo](?path=docs/schemas-md/IdInfo.md)|
| agentId | ``` string ```  *maxLength: 6 pattern: (?=.*[^\s])^[^|]+$ example: RVK001* Used to track the agent transaction activity.|
| terminalId | ``` string ```  *maxLength: 10 pattern: ^[0-9]+$ example: 1283673312* Identifies the register or lane number where the original sale transaction occurred.|
| registrationId | ``` string ```  *maxLength: 50 pattern: (?=.*[^\s])^[^|]+$ example: 12345* Unique ID assigned by the merchant for the consumer (never recycled). It is an additional level of authentication. To use this feature, the merchant must work with TeleCheck Risk to discuss. Registration IDs must not be generated for an existing or returning consumer returns. The single registration ID must be unique per consumer.|
| registrationDate | ``` string ```  *($date) example: 2019-10-02* Date the consumer originally registered in format MMDDYYYY.|
| releaseType | ``` string ```  *example: P* Release type is used as a risk variable to gauge risk level when the merchant is releasing the purchased merchandise. Enum:[ C, D, P, T ]|
| vipCustomer | ``` string ```  *example: Y* Flags a transaction as a VIP order (based on merchant criteria). This field should not be sent for non-VIP orders. Enum:[ Y, N ]|
| sessionId* | ``` string ```  *maxLength: 128 pattern: (?=.*[^\s])^[^|]+$ example: fb2e77d.47a0479900504cb3ab4a1f626d174d2d* Session identifier.|
| terminalState | ``` string ```  *maxLength: 2 pattern: ^[A-Z]{2}$ example: GA* Identifies the US state or territory where the original sale transaction occurred.|
| terminalCity | ``` string ```  *maxLength: 16 pattern: (?=.*[^\s])^[^|]+$ example: Atlanta* Identifies the city where the original sale transaction occurred.|
| achBillTo |{ [achBillTo](?path=docs/schemas-md/AchBillTo.md) }|  
| customerIpAddress | ``` string ```  *maxLength: 15 pattern: ^[0-9\.]+$ example: 11.32.232.44* Customer IP address from the terminal where the order was placed (as captured by merchant).|
| recurringType | [AchRecurringType](?path=docs/schemas-md/AchRecurringType.md)|  


**TeleCheckICAPaymentMethod Example:**

```{r}

{
  "achType": "TeleCheckICAPaymentMethod",
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
  "customerIpAddress": "11.32.232.44",
  "imeiCode": "99-000086-247185-4",
  "recurringType": "Single"
}
```






# Disbursement

| *description*:   | *Disbursement information. Abstract class, do not use this class directly, use one of its children: FundingTransactionType, DisbursementTransactionType*|US MIDs|Non-US MIDs|
|----|----|----|----|
| disbursementType |    ``` string ```  <br/>  *example: FundingTransactionType*  <br/> The type of disbursement.|Visa: Mandatory for AFT transactions<br/>MC: Mandatory for funding transactions|Visa: Mandatory for AFT transactions<br/>MC: Mandatory for funding transactions|
| fundingSource |    ``` string ```  <br/>  *example: CREDIT_ACCOUNT*|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|
| senderInfo | [SenderInfo](?path=docs/schemas-md/SenderInfo.md)|Visa: Optional for AFT transactions <br/>MC: Optional for funding transactions|Visa: Mandatory for AFT transactions<br/>MC: Optional for funding transactions|
| receiverInfo | [ReceiverInfo](?path=docs/schemas-md/ReceiverInfo.md)|Visa: Optional for AFT transactions <br/>MC: Mandatory for funding transactions|Visa: Mandatory for AFT transactions<br/>MC: Mandatory for funding transactions|

**Disbursement Example:**

```{r}

{
  "disbursementType": "DisbursementTransactionType",
  "fundingSource": "CREDIT_ACCOUNT",
  "senderInfo": {
    "name": "Franklin Sender Roosevelt",
    "streetAddress": "5565 Glenridge Connector",
    "city": "Atlanta",
    "stateCode": "GA",
    "countryCode": "US",
    "postalCode": "30342",
    "phoneNumber": "4044040740",
    "birthDate": "19560121",
    "participationId": "123456789123456789123456789123",
    "referenceNumber": "12345678",
    "accountNumber": "135246",
    "accountType": "CARD_ACCOUNT_NO"
  },
  "receiverInfo": {
    "name": "Abraham Receiver Lincoln",
    "streetAddress": "5565 Glenridge Connector",
    "city": "Atlanta",
    "stateCode": "GA",
    "countryCode": "US",
    "postalCode": "30342",
    "phoneNumber": "4044040740",
    "referenceNumber": "12345678",
    "accountNumber": "135246",
    "accountType": "ROUTING_TRANSIT_NO_AND_BANK_ACCOUNT_NO"
  }
}
``` 


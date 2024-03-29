
# Disbursement

| *description*:   | *Disbursement information. Abstract class, do not use this class directly, use one of its children: FundingTransactionType, DisbursementTransactionType*|
|----|----|
| disbursementType |    ``` string ```  <br/>  *example: FundingTransactionType*  <br/> The type of disbursement.|
| senderInf* | [SenderInfo](?path=docs/schemas-md/SenderInfo.md)|
| receiverInfo* | [ReceiverInfo](?path=docs/schemas-md/ReceiverInfo.md)|

**Disbursement Example:**

```{r}

{
  "disbursementType": "DisbursementTransactionType",
  "senderInfo": {
    "name": "Franklin Sender Roosevelt",
    "streetAddress": "5565 Glenridge Connector",
    "city": "Atlanta",
    "stateCode": "GA",
    "countryCode": "US",
    "postalCode": "30342",
    "phoneNumber": "4044040740",
    "birthDate": "19560121",
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

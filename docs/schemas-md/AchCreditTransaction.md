
# AchCreditTransaction

| *description*:   | *Request to create Credit primary transaction using ACH telecheck details.*|
|----|----|
| requestType |    ``` string ```  *example:   PaymentCardCreditTransaction*. Object name of the primary transaction request.|
| transactionAmount | [Amount](?path=docs/schemas-md/Amount.md)|
| storeId |    ``` string ```  *maxLength: 20  example: 12345500000*. An optional outlet ID for clients that support multiple stores in the same app.|
| merchantTransactionId |    ``` string ```   * maxLength: 40 example: lsk23532djljff3*. The unique merchant transaction ID from the request, if supplied.|
| transactionOrigin |  TransactionOrigin  ``` string ```  *example: ECOM*.The source of the transaction. The possible values are ECOM (if the order was received via email or Internet), MOTO (mail order, telephone order), MAIL, PHONE and RETAIL (face to face). Enum:Array [ 5 ] - [ ECOM, MOTO, MAIL, PHONE, RETAIL ]|
| order | [Order](?path=docs/schemas-md/Order.md)|
| ipgTransactionId |    ``` integer ``` ($int64)  *example: 838916029301*. The response transaction ID.|
| allowPartialApproval |    ``` boolean ```  *example: true*. Indicates if the particular transaction is a partial approval transaction, if supplied.|
| paymentMethod | [TeleCheckAchPaymentMethod](?path=docs/schemas-md/TeleCheckAchPaymentMethod.md)|

**AchCreditTransaction Example:**

```{r}

{
  "requestType": "AchCreditTransaction",
  "transactionAmount": {
    "total": 12.04,
    "currency": "USD"
  },
  "paymentMethod": {
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
    "organizationId": "XXXXXXXXXXXXXX",
    "sessionId": "XXXXXXXXXXXXXX",
    "terminalState": "GA",
    "terminalCity": "Atlanta",
    "customerIpAddress": "11.32.232.44",
    "imeiCode": "990000862471854"
  }
}
``` 

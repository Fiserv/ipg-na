
# ReferencedOrderPaymentTokenizationRequest

| *description*:   | *Used to generate payment tokens with an existing order ID.*|
|----|----|
| requestType |    ``` string ```  <br/>  *example: PaymentCardVerificationRequest* <br/> Object name of the account verification request.|
| storeId |    ``` string ```  <br/> maxLength: 20   <br/> *example: 12345500000* <br/>  An optional outlet ID for clients that support multiple stores in the same app.|
| billingAddress |  [Address](?path=docs/schemas-md/Address.md)|  
| createToken | [CreatePaymentToken](?path=docs/schemas-md/CreatePaymentToken.md)|     
| accountVerification |  ``` boolean ```  <br/> default: false  <br/> *example: true* <br/>  If the account should be verified prior to token creation.|
| merchantTransactionId |    ``` string ```   <br/> maxLength: 40  <br/> *example: lsk23532djljff3* <br/> The unique merchant transaction ID from the request, if supplied.|
| additionalDetails | [AdditionalDetails](?path=docs/schemas-md/AdditionalDetails.md)|
| referencedOrderId |  ``` string ```  <br/> pattern: ^(?!\s*$).+   <br/> *example: R-f9c2c198-b7cc-491a-a711-93d22fd0e589*  <br/> Order ID used to create recurring payment from existing transaction.|  

**ReferencedOrderPaymentTokenizationRequest Example:**

```{r}

{
  "requestType": "ReferencedOrderPaymentTokenizationRequest",
  "createToken": {
    "value": "234ljl124l12",
    "reusable": true,
    "declineDuplicates": false
  },
  "referencedOrderId": "R-f9c2c198-b7cc-491a-a711-93d22fd0e589",
  "accountVerification": true
}
```




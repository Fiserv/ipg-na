
# Level2

| *description*: | *Level 2 data for monitoring and controlling corporate expenditures.*|
|----|----|
| customerReferenceID |    ``` string ```  <br/>   *maxLength: 17 	 <br/> example: abcdef123xyz* 	 <br/> Customer code/customer reference ID. The max length supported for Visa is 12 and MasterCard is 17.|
| supplierInvoiceNumber |    ``` string ```   <br/>  *maxLength: 30  <br/>  example: 0000000065348*   <br/> Purchase identifier/merchant-related data.|
| supplierVATRegistrationNumber |    ``` string ```  <br/>   *maxLength: 30  <br/> example: 10001174242* 	 <br/> Merchant VAT registration/single business reference number/merchant tax ID or corporation VAT number.|
| totalDiscountAmountAndRate | [AdditionalAmountRate](?path=docs/schemas-md/AdditionalAmountRate.md)|
| vatShippingAmountAndRate | [AdditionalAmountRate](?path=docs/schemas-md/AdditionalAmountRate.md)|
| dutyAmountAndRate | [AdditionalAmountRate](?path=docs/schemas-md/AdditionalAmountRate.md)|

**Level2 Example:**

```{r}

{
    "customerReferenceID": "abcdef123xyz",
    "supplierInvoiceNumber": "0000000065348",
    "supplierVATRegistrationNumber": "10001174242",
    "totalDiscountAmountAndRate": {
      "amount": 5.145,
      "rate": 1.175
    },
    "vatShippingAmountAndRate": {
      "amount": 6.03,
      "rate": 1.175
    },
    "dutyAmountAndRate": {
      "amount": 7.03,
      "rate": 1.175
    }
}
```  







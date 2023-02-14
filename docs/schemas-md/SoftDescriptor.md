
# SoftDescriptor

| *description*:   | *Identifying information about a merchant which appears on buyer's credit/debit card statements.*|
|----|----|
| dynamicMerchantName* |    ``` string ```  *pattern: ^(?!\s*$).+ example: Merchant XYZ* Store "doing-business-as" name.|
| customerServiceNumber |    ``` string ```  *maxLength: 10 pattern: ^[0-9]+$ example: 9973322990* Customer service phone number information that is passed to the issuer (it may appear on the cardholder’s statement) or if merchant wants to pass information that differs from the information stored on our master File.|
| mcc |   ``` string ```  *maxLength: 4 example: 7311* The 4-digit merchant category code (MCC). The merchant might be associated with multiple MCCs. In that case the MCC provided here will be the one that better describes the current transaction.|
| dynamicAddress |  [Address](?path=docs/schemas-md/Address.md)|        

**SoftDescriptor Example:**

```{r}

{
  "dynamicMerchantName": "Merchant XYZ",
  "customerServiceNumber": "8045018787",
  "mcc": "7311",
  "dynamicAddress": {
    "company": "XYZ Company",
    "address1": "5565 Glenridge Conn",
    "address2": "Dundwoody Area",
    "city": "Atlanta",
    "region": "Georgia",
    "postalCode": "30342",
    "country": "USA"
  }
}

``` 

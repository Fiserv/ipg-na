
# CardholderInfoResponse

| *description*: | *The processor Cardholder Info Response.*| 
|----|----|
| postalCodeOrZipMatch |  ``` string ``` <br/> *example: Y*  <br/> Response if card holder postal code matches that on file.|
| addressMatch |  ``` string ```  <br/>  *example: RETRY* <br/>  Response if card holder address matches that on file.|
| nameMatch |  ``` string ```  <br/>  *example: SERVICE_NOT_ALLOWED* <br/>  Response if card holder name matches that on file.|
| telephoneMatch |  ``` string ``` <br/>   *example: NOT_CHECKED*  <br/> Response if card holder telephone matches that on file.|
| emailMatch |  ``` string ```  <br/>  *example: N*  <br/> Response if card holder email matches that on file.|
| associationCardholderInfoResponse |  ``` string ```  <br/>  *example: YNUSR*  <br/> Raw cardholder info response from AMEX with no mapping.|   






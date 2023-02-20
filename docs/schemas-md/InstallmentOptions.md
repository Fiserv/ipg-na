
# InstallmentOptions

| *description*: | *Indicates that the total sum payable is divided for payment at successive fixed times.*|
|----|----|
| numberOfInstallments |    ``` integer ```   <br/>  *($int32) <br/>  minimum: 1  <br/> maximum: 99  <br/> example: 5*  <br/> Number of instalments for a sale transaction if the customer pays the total amount in multiple transactions.|
| installmentsInterest |    ``` boolean ```  <br/>   *example: true*  <br/> Indicates whether the installment interest amount has been applied.|
| installmentDelayMonths |    ``` integer ```   <br/>  *($int32) <br/>  minimum: 1 <br/>  maximum: 99   <br/> example: 5*  <br/> The number of months the first installment payment will be delayed.|
| recurringType |    ``` string ```  <br/>   *example: FIRST*  <br/> The type of recurring payment.  <br/> Enum:[ FIRST, REPEAT, STANDING_INSTRUCTION ]|
| merchantAdviceCodeSupported |    ``` boolean ```   <br/>  *example: true* <br/>  Indicates if the merchant supports merchant advice code (MAC) in order to receive table 55 code for a declined recurring transaction.|

**InstallmentOptions Example:**

```{r}

{
  "numberOfInstallments": 5,
  "installmentsInterest": true,
  "installmentDelayMonths": 5,
  "recurringType": "FIRST",
  "merchantAdviceCodeSupported": true
}
```  







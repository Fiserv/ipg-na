
# InstallmentOptions

| *description*: | *Indicates that the total sum payable is divided for payment at successive fixed times.*|
|----|----|
| numberOfInstallments |    ``` integer ```   *($int32) minimum: 1 maximum: 99 example: 5* Number of instalments for a sale transaction if the customer pays the total amount in multiple transactions.|
| installmentsInterest |    ``` boolean ```   *example: true* Indicates whether the installment interest amount has been applied.|
| installmentDelayMonths |    ``` integer ```   *($int32) minimum: 1 maximum: 99  example: 5* The number of months the first installment payment will be delayed.|
| recurringType |    ``` string ```   *example: FIRST* The type of recurring payment. Enum:[ FIRST, REPEAT, STANDING_INSTRUCTION ]|
| merchantAdviceCodeSupported |    ``` boolean ```   *example: true* Indicates if the merchant supports merchant advice code (MAC) in order to receive table 55 code for a declined recurring transaction.|

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








# PaymentMethodDetails

| *description*:   | *Provides details of the payment method used.*|
|----|----|
| paymentCard* |  [PaymentCard](?path=docs/schemas-md/PaymentCard.md)|
| paymentMethodType |  PaymentMethodType   <br/> ``` string ```  <br/>  *example: DEBITDE*  <br/> Type of payment method.  <br/> Enum:Array [ 39 ] - [ ALIPAY, ALIPAY_PAYSECURE_US, ALIPAY_DOMESTIC, APM, BCMC, BITPAY, BLIK, BOLETO, CASH, CONEKTA, CUP_DOMESTIC, DEBITDE, EMI, EPS, GIROPAY, IDEAL, INDIAWALLET, KLARNA, KPS, MYBANK, NATWEST_PAYIT, NETBANKING, PAYMENT_CARD, PAYMENT_TOKEN, PAYPAL, PAYSAFECARD, POLI, POSTFINANCE_CARD, POSTFINANCE_EF, PRZELEWY24, SAFETYPAY, SEPA, SOFORT, TELECHECK, TRUSTLY, TRUSTPAY, WALLET, WECHAT, WECHAT_DOMESTIC ]|

**PaymentMethodDetails Example:**

```{r}

{
  "paymentCard": {
    "number": "5424180279791732",
    "expiryDate": {
      "month": "12",
      "year": "25"
    },
    "securityCode": "977"
  },
  "paymentMethodType": "PAYMENT_CARD"
}
``` 






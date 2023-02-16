
# ApmPaymentMethod

| *description*:   | *Payment method containing APM specific information, which is intentionally weakly-typed to allow for reduced coupling of APM plugins.*|
|----|----|
| type* |    ``` string ```  <br/> Type of payment method.  <br/> Enum:Array [ 5 ] - [ BLIK, NATWEST_PAYIT, POSTFINANCE_CARD, POSTFINANCE_EF, PAYPAL ]|
| paymentToken* |    ``` string ``` <br/>  pattern: [A-Za-z0-9]{1,128}.  <br/> Only applicable for type: PAYPAL. Token/HostedDataId that has been created for the user account.| 


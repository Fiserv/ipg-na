
# ApmPaymentMethod

| *description*:   | *Payment method containing APM specific information, which is intentionally weakly-typed to allow for reduced coupling of APM plugins.*|
|----|----|
| type* |    ``` string ``` Type of payment method. Enum:Array [ 5 ] - [ BLIK, NATWEST_PAYIT, POSTFINANCE_CARD, POSTFINANCE_EF, PAYPAL ]|
| paymentToken* |    ``` string ``` pattern: [A-Za-z0-9]{1,128}. Only applicable for type: PAYPAL. Token/HostedDataId that has been created for the user account.| 


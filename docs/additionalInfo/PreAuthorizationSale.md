
# Pre-Authorization/Sale


## Step 1: Checkout Process in Your Webstore

The easiest first step for adding payments capabilities to your website is to implement a HTML form that you post to our Gateway URL.

This type of integration allows you to let our Gateway manage the customer redirections that are required in the checkout process of many payment methods or authentication mechanisms and gives you the option to use secure hosted pages or an embeddable form which can reduce the burden of compliance with the Data Security Standard of the Payment Card Industry (PCI DSS).

With the transaction type Pre-Authorization (preauth) you can reserve funds on a customer's card account. This transaction does not charge the card until you perform a Completion transaction. Note that pre-authorizations reserve funds for varying periods, depending on the issuing card company's policy. We strongly suggest that you confirm shipment as soon as possible after authorization.

Alternatively you can use the transaction type Sale (sale) which immediately charges a customer�s card or bank account over night with no further action required from you.
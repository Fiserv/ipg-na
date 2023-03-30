
# Online Store Integration


### Adding Payment Capabilities to a Website

The easiest way to add payment capabilities to your website is to implement a HTML form that you post to our Gateway URL.

This type of integration allows you to let our Gateway manage the customer redirections that are required in the checkout process of many payment methods or authentication mechanisms and gives you the option to use secure hosted pages which can reduce the burden of compliance with the Data Security Standard of the Payment Card Industry (PCI DSS).

***Important Note:  When making decisions on your way of integration, please consider that we do not recommend to use the hosted payment forms inside an iFrame since some Internet browsers do not allow cookies to be sent to the 3rd party hosts, moreover some features (e.g.: 3D Secure authentications) and some Alternative Payment methods that involve redirections to the 3rd party services (e.g. iDEAL or PayPal) do not allow displaying their screens within an iFrame. However, if you still plan to embed our hosted payment pages inside an iFrame you must use the 'parentUri' parameter to specify an URL of a page, where the hosted payment page will be embedded.***

### Application Programming Interface

For steps where no direct consumer interaction is required and no sensitive cardholder data is getting processed, it's best to use our [Application Programming Interface (API)](https://developer.fiserv.com/product/IPGNA/api/?type=post&path=/authentication/access-tokens&branch=main&version=1.0.0). Please note that if you plan to collect your customer's card details within your environment and send it to our API, you must ensure that your system components are PCI DSS compliant.

### Key Steps

The following five steps provide an overview of a standard online store integration with links to alternative options where applicable:

> Step 1: [Checkout Process in Your Webstore (Pre-Authorization or Sale)](?path=docs/additionalInfo/PreAuthorizationSale.md)
 
> Step 2: [Receiving the Transaction Result](?path=docs/additionalInfo/TransactionResponse.md)
 
> Step 3: [Completion When Goods Get Shipped (Post-Authorization)](?path=docs/additionalInfo/Completion.md)
 
> Step 4: [Voiding a Transaction](?path=docs/additionalInfo/Void.md)

> Step 5: [Giving Money Back When Goods Have Been Returned (Refund)](?path=docs/additionalInfo/Return.md)
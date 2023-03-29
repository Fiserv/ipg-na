
# Pre-Authorization/Sale


## Step 1: Checkout Process in Your Webstore

The easiest first step for adding payments capabilities to your website is to implement a HTML form that you post to our Gateway URL.

This type of integration allows you to let our Gateway manage the customer redirections that are required in the checkout process of many payment methods or authentication mechanisms and gives you the option to use secure hosted pages or an embeddable form which can reduce the burden of compliance with the Data Security Standard of the Payment Card Industry (PCI DSS).

With the transaction type **Pre-Authorization** (preauth) you can reserve funds on a customer's card account. This transaction does not charge the card until you perform a Completion transaction. Note that pre-authorizations reserve funds for varying periods, depending on the issuing card company's policy. We strongly suggest that you confirm shipment as soon as possible after authorization.

Alternatively you can use the transaction type **Sale** (sale) which immediately charges a customer�s card or bank account over night with no further action required from you.

## Integration Options

> - Fully outsource the payment process using Hosted Payment Pages
> - Full control over the look and feel using a Direct Post

## Alternative Options
> API-only integration
> Tokenize card details with JavaScript

## What You Need

When using the Direct Post or Hosted Payment Pages options, you need:

> - Store Name (storename)
	This is the ID of the store that was given to you by First Data. For example : 10123456789
 
> - Shared Secret
	This is the shared secret provided to you by First Data. This is used when constructing the hash value.

## URL for Test Transactions

https://test.ipg-online.com/connect/gateway/processing
You will get the production URL with your production account credentials.

## Building the Request

Independently of the payment method, there are some mandatory fields that need to be included in your transaction request:

| *Field* | *Comment*|
|----|----|
|txntype|The type of the transaction: preauth, sale or payer_auth (see info on payer_auth here)|
|timezone|The timezone of the transaction in Area/Location format,<br/>e.g. America/New_York  or Europe/Berlin|
|txndatetime|The exact time of the transaction in format<br/>YYYY:MM:DD-hh:mm:ss|
|hash_algorithm|This is to indicate the algorithm that you use for hash calculation. Valid values are: HMACSHA256 or HMACSHA384 or HMACSHA512|
|hashExtended|The extended hash needs to be calculated using all request parameters in ascending order of the parameter names.<br/>When you are using Direct Post, there is also an option where you do not need to know the card details (PAN, CVV and Expiry Date) for the hash calculation. This will be managed with a specific setting performed on your store. Please contact your local support team if you want to enable this feature.|
|storename|The ID of the store provided to you by First Data, e.g. 541234567|
|chargetotal|The total amount of the transaction using a dot or comma as decimal separator, e.g. 12.34 for an amount of 12 Dollar and 34 Cents. Group separators like 1,000.01 / 1.000,01 are not allowed.|
|currency|The numeric ISO code of the transaction currency <br/>e.g. 840 for US Dollar or 978 for Euro|

## Sample Code for Your Checkout Form

Example of a form with the minimum number of fields:

```

<form method="post" action="https://test.ipg-online.com/connect/gateway/processing">
  <input type="hidden" name="txntype" value="preauth">
  <input type="hidden" name="timezone" value="Europe/Berlin">
  <input type="hidden" name="txndatetime" value="<% getDateTime() %>"/>
  <input type="hidden" name="hash_algorithm" value="HMACSHA256"/>
  <input type="hidden" name="hashExtended" value="<% call createExtendedHash( "13.00","978" ) %>"/>
  <input type="hidden" name="storename" value="10123456789">
  <input type="text" name="chargetotal" value="13.00">
  <input type="hidden" name="currency" value="978">
  <input type="submit" value="Submit">
</form>

```

> [How to generate a hash](?path=docs/additionalInfo/HowToGenerateHash.md)

> [Values for defining the payment method](?path=docs/additionalInfo/PaymentMethodValues.md)

> [Parameters for billing/shipping information](?path=docs/additionalInfo/BillingShippingFields.md)

## Next Steps

> [Transaction Response](?path=docs/additionalInfo/TransactionResponse.md)

> [Completion (Post-Authorization)](?path=docs/additionalInfo/Completion.md)

> [Void](?path=docs/additionalInfo/Void.md)

> [Return](?path=docs/additionalInfo/Return.md)
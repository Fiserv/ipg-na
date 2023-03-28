
# Pre-Authorization/Sale


## Step 1: Checkout Process in Your Webstore

The easiest first step for adding payments capabilities to your website is to implement a HTML form that you post to our Gateway URL.

This type of integration allows you to let our Gateway manage the customer redirections that are required in the checkout process of many payment methods or authentication mechanisms and gives you the option to use secure hosted pages or an embeddable form which can reduce the burden of compliance with the Data Security Standard of the Payment Card Industry (PCI DSS).

With the transaction type **Pre-Authorization** (preauth) you can reserve funds on a customer's card account. This transaction does not charge the card until you perform a Completion transaction. Note that pre-authorizations reserve funds for varying periods, depending on the issuing card company's policy. We strongly suggest that you confirm shipment as soon as possible after authorization.

Alternatively you can use the transaction type **Sale** (sale) which immediately charges a customer’s card or bank account over night with no further action required from you.

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



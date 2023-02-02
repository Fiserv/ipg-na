
# Google Pay

Google Pay is the fast, simple way to pay in millions of places – online, in stores, and more. It brings together everything you need at checkout and keeps your information safe and secure.

**User Action**: the buyer taps the "Google Pay" button, and then selects a payment method and shipping address.

## If the purchase originates from a third-party site

	1. The merchant/client server issues a credential request with the Merchant ID and Processor Name as First Data to Google.
	2. Google returns response with encrypted payment credentials signed with the First Data key to the merchant server.
	3. The Merchant sends the encrypted payload to First Data.
	4. First Data decrypts and validates the payload, and then processes the transaction and responds back to merchant with either an approval or decline response.

## If the purchase originates from a Google site:

	1. Google initiates a purchase request to the merchant after the consumer confirms order.
	2. The merchant/client server issues a request with the Merchant ID and Processor Name as First Data to Google.
	3. Google returns response with encrypted payment credentials signed with the First Data key to merchant server.
	4. The merchant sends the encrypted payload to First Data.
	5. First Data decrypts and validates the payload and process the transaction and respond back to merchant with either an approval or decline response.
 
 
To get more information on participating banks and countries for Google Pay, click here.


## Google Pay Integration

## Overview

Google Pay enables developers to add payment processing to merchants’ Android-compatible apps and on Chrome on Android. These APIs allow consumers to pay with any credit card they have stored in their Google account, including any cards they may have previously set up on their Android Pay digital wallet. Consumers may also add a new payment account.

The target audience for this document is a developer who wants to use Google Pay in their payment application.

 

## Merchant Boarding

Please reach out to your local Integration Support team for getting your account enabled.

## Prerequisites to build and run the sample Application

# Direct Post


Using Direct Post allows you to have full control over the look and feel of the form where your customers enter their card details for payment while simultaneously avoiding the need to have sensitive card data within your systems.

You create the payment form and display it within your website or app. When your customer has entered the card details and presses the "continue button", the customer's device sends the payment information directly to Fiserv.

This comes with many advantages and benefits to you with regard to both the customer experience, and your overall PCI Data Security Standard compliance exposure.



If you choose the Direct Post option and create your own forms, there are additional fields that must be included in your transaction requests. The available options are listed below. It is also important that you check that JavaScript is enabled in your customer's browser. If necessary, inform your customer that JavaScript needs to be enabled for the payment process.

## Required Fields

After your customer has decided on his/her payment method, you present a corresponding HTML-page with a form to enter the payment data as well as hidden parameters containing additional transaction information. In addition to any mandatory fields, your form must contain the following fields (some of which can be hidden) to use the Direct Post option:

| *Field*: | *Comment*|
|----|----|
|paymentMethod|If you let the customer select the payment method (e. g. MasterCard, Visa, Direct Debit) in your shop environment or want to define the payment type yourself, transmit the parameter 'paymentMethod' along with your Sale or PreAuth transaction.<br/>If you do not submit this parameter, the payment gateway will display a drop-down menu to the customer to choose from the payment methods available for your shop.<br/><br/> > [See valid values here](?path=docs/additionalInfo/PaymentMethodValues.md)|
|responseFailURL|	The URL where you wish to direct customers after a declined or unsuccessful transaction (your Sorry URL), only needed if not setup in Virtual Terminal / Customization.|
|responseSuccessURL	|	The URL where you wish to direct customers after a successful transaction (your Thank You URL), only needed if not setup in Virtual Terminal / Customization.|

## For Credit/Debit Card Details

| *Field*: | *Comment*|
|----|----|
|cardnumber|Your customer's card number (12-24 digits)|
|expmonth|Card expiry month (2 digits) (mandatory if credit card)|
|expyear|Card expiry year (4 digits) (mandatory if credit card)|
|cvm|Card code, usually back of the card (3/4 digits) (mandatory if credit card) (optional "if on card") (not needed for Bancontact)|

## For SEPA Direct Debit Details

| *Field*: | *Comment*|
|----|----|
|iban|International bank account number (up to 34 digits)|
|bname|Name of bank account owner|
|baddr1	|Mandatory if IBAN belongs to EFTA and associated country. Street name and house number of the bank account owner that will be debited (alphanumeric characters, spaces, and dashes limited to 96 characters)|
|bcity|Mandatory if IBAN belongs to EFTA and associated country. City of the bank account owner that will be debited (alphanumeric characters, spaces, and dashes limited to 96 characters)|
|bcountry|Mandatory if IBAN belongs to EFTA and associated country. Country of the bank account owner that will be debited (2 letter country code)|
|bzip|Mandatory if IBAN belongs to EFTA and associated country. Zip or postal code of the bank account owner that will be debited (limit of 24 characters incl. spaces)|

You can also transfer [billing and shipping](?path=docs/additionalInfo/BillingShippingFields.md) information to the Gateway.

> [See other optional fields that might be useful for your business](?path=docs/additionalInfo/OtherOptionalFields.md)

## Validity Checks

Prior to the authorization request for transactions, the Gateway performs the payment methods' specific validation checks.

For Credit/Debit Card or SEPA Direct Debit transactions the following checks are performed:

> - Expiry date of the cards must be in the future
> - Card security codes must contain 3 or 4 digits
> - Structure of the card number must be correct
> - Name of the account holder for SEPA Direct Debit transactions must be submitted
> - IBAN for SEPA Direct Debit transactions must be correct and contain up to 34 digits
> - If an IBAN belongs to one of the following countries: Andorra, Switzerland, United Kingdom (incl. Jersey, Guernsey, Isle of Man), Gibraltar, Iceland, Liechtenstein, Monaco, Norway, San Marino, Vatican City, then the account holder's address details must be submitted.

If the submitted data is invalid, the Gateway would usually send a corresponding data entry page to the customer. However, using the silent post feature, you can transmit an additional parameter along with transaction data: 'full_bypass=true'. In this case, you get the result of the validity check back in the transaction response and can display your own error page.

## Sample Code for the HTML Form

```
<form method="post" action="https://test.ipg-online.com/connect/gateway/processing">

<!-- Hidden fields to be prefilled by the merchant -->   
   <input type="hidden" name="full_bypass" value="true">
   <input type="hidden" name="txntype" value="sale">
   <input type="hidden" name="paymentMethod" value="V">
   <input type="hidden" name="timezone" value="Europe/Berlin">
   <input type="hidden" name="txndatetime" value="<?php echo getDateTime() ?>">
   <input type="hidden" name="hash_algorithm" value="HMACSHA256">
   <input type="hidden" name="hashExtended" value="<?php echo createExtendedHash( "13.00","978" ) ?>">
   <input type="hidden" name="storename" value="10123456789">
   <input type="hidden" name="chargetotal" value="13.00">
   <input type="hidden" name="currency" value="978">
   <input type="hidden" name="language" value="en_US">

<!-- Fields to be entered by the cardholder -->
 <div>
   <!-- credit card number: e.g. 4111111111111111 -->
   <label for="cardnumber">Card Number:</label>
   <input type="text" name="cardnumber" id="cardnumber">
 </div>

 <div>
   <!-- expiration month of the card: e.g. 07 -->   
   <label for="expmonth">Expiration Month:</label>
   <input type="text" name="expmonth" id="expmonth">
 </div>

 <div>
   <!-- expiration year of the card: e.g. 2024 -->
   <label for="expyear">Expiration Year:</label>
   <input type="text" name="expyear" id="expyear">
 </div>

 <div>
   <!-- card security code (CVV/CVC): e.g. 123 -->
   <label for="cvm">Security Code:</label>
   <input type="text" name="cvm" id="cvm">
 </div>

 <div>
   <input type="submit" value="Submit">Pay now</input>
 </div>

</form>

```
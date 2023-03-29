
# Optional HTML Form Fields


If you post a HTML form to initiate the payment, there are a number of optional fields that you can include in your request for different purpose.

### Checkout Experience Related Fields

| *Field*: | *Comment*|
|----|----|
| hideOrderDetails | Set this parameter to **true** when you want to remove the Your Order box from our hosted page in the checkout option **combinedpage**. |
|idealIssuerID |This parameter can be used to submit the iDEAL issuing bank in case you let your customers select the issuer within your shop environment. If you do not pass this value for an iDEAL transaction, a hosted selection form will be displayed to your customer, from Table below  **TABLE1**|
|language|This parameter can be used to override the default payment page language configured for your merchant store. The following values are currently possible, from below **TABLE2**|
| parentUri | If you plan to embed our hosted payment pages inside an iFrame you must use this parameter, with the maximum length of 2048 characters, to specify an URL of a page, where the hosted payment page will be embedded. However, note that we do not recommend using the hosted payment forms inside an iFrame since some Internet browsers do not allow cookies to be sent to the 3rd party hosts, moreover some features (e.g.: 3D Secure authentications) and some Alternative Payment methods that involve redirections to the 3rd party services (e.g.: iDEAL or PayPal) do not allow displaying their screens within an iFrame. |
| paymentMethod | If you let the customer select the payment method (e. g. MasterCard, Visa, Direct Debit) in your shop environment or want to define the payment type yourself, transmit the parameter **paymentMethod** along with your Sale or PreAuth transaction. If you do not submit this parameter, the payment gateway will display a drop-down menu to the customer to choose from the payment methods available for your shop. [See valid values here](?path=docs/additionalInfo/OtherOptionalFields.md)|
| responseFailURL | The URL where you wish to direct customers after a declined or unsuccessful transaction (your Sorry URL) – only needed if not setup in Virtual Terminal / Customization. |
| responseSuccessURL | The URL where you wish to direct customers after a successful transaction (your Thank You URL) – only needed if not setup in Virtual Terminal / Customization. |

#### TABLE1 :

| *Field*: | *Comment*|
|----|----|
|ABN AMRO|ABNANL2A|
|ING|INGBNL2A|
|SNS Bank|SNSBNL2A|
|van Lanschot|FVLBNL22|
|Triodos Bank|TRIONL2U|
|Knab|KNABNL2H|
|Rabobank|RABONL2U|
|RegioBank|RBRBNL21|
|ASN Bank|ASNBNL21|
|Bunq|BUNQNL2A|
|Handelsbanken|HANDNL2A|
|Moneyou|MOYONL21|
|Revolut|REVOLT21|

#### TABLE2 :

| *Language*: | *Value*|
|----|----|
|Chinese (simplified)|zh_CN
|Chinese (traditional)|zh_TW|
|Czech|cs_CZ|
|Danish|da_DK|
|Dutch|nl_NL|
|English (USA)|en_US|
|English (UK)|en_GB|
|Finnish|fi_FI|
|French|fr_FR|
|German|de_DE|
|Greek|el_GR|
|Hungarian|hu_HU|
|Italian|it_IT|
|Japanese|ja_JP|
|Norwegian (Bokmål) |nb_NO|
|Polish|pl_PL|
|Portuguese (Brazil)|pt_BR|
|Serbian (Serbia)|sr_RS|
|Slovak|sk_SK|
|Slovenian |sl_SI|
|Spanish (Spain)|es_ES|
|Spanish (Mexico)|es_MX|
|Swedish|sv_SE|

### Transaction Identifiers

| *Field*: | *Comment*|
|----|----|
|merchantTransactionId|Allows you to assign a unique ID for the transaction with up to 40 characters. This ID can be used to reference to this transactions in a PostAuth or Void request (referencedMerchantTransactionId).|
|oid|This field allows you to assign a unique ID for your order with up to 100 characters. If you choose not to assign an order ID, the Fiserv system will automatically generate one for you. Please note that for Direct Debit transactions, a maximum of 78 characters can be submitted to the bank.|
|referencedMerchantTransactionID|This field allows to reference to a merchantTransactionId of a transaction when performing a Void. This can be used as an alternative to ipgTransactionId if you assigned a merchantTransactionId in the original transaction request.|

### Consumer Information

| *Field*: | *Comment*|
|----|----|
|customerid |Please note that for: <br/> Direct Debit transactions, the Customer ID can be submitted to the bank with the maximum length of 32 characters. The minimum length of the Order ID is 32 characters, but it can be longer if the Customer ID is shorter. The maximum amount of characters for both Customer ID and Order ID that can be submitted to the bank is 64. Please contact your local support team if you want to enable this feature but note that this is not applicable when processing Direct Debit through the Fiserv Local Payments offering.<br/>iDEAL transactions, the Customer ID can be submitted in your request filled in with any relevant data which can be populated in a field in the iDEAL TransactionRequest to be displayed on your consumers** bank account statements. Please note that this is not applicable when processing iDEAL through the Fiserv Local Payments offering.|

### Card Related Fields

| *Field*: | *Comment*|
|----|----|
|ponumber|This field allows you to submit a Purchase Order Number with up to 50 characters.|

### Additional Transaction Information

| *Field*: | *Comment*|
|----|----|
|comments|Place any comments here about the transaction.|
|dynamicMerchantName|The name of the merchant to be displayed on the cardholder**s statement. The length of this field should not exceed 25 characters. If you want to use this field, please contact your local support team to verify if this feature is supported in your country.|
|invoicenumber|This field allows you to transmit any value, e. g. an invoice number or class of goods. Please note that the maximum length for this parameter is 48 characters.|
|item1 up to item999|Line items are regular key-value parameters (URL-encoded), where:<br/> 1. the name is a combination of the keyword item and a number, where the number indicates the list position e.g.: item1<br/> 2. the value is represented by a semicolon-separated list of values, where the position indicates the meaning of the list item property e.g.: <1>;<2>;<3>;<4>;<5>;<6>;<7><br/> The **item1** to **item999** parameters allow you to send basket information in the following format:<br/> **id;description;quantity;item_total_price;sub_total;vat_tax;shipping**|
|shipping|This parameter can be used to submit the shipping fee, in the same format as **chargetotal**. If you submit **shipping**, the parameters **subtotal** and **vattax** have to be submitted as well. Note that the **chargetotal** has to be equal to **subtotal** plus **shipping** plus **vattax**.|
|trxOrigin|This parameter allows you to use the secure and hosted payment form capabilities within your own application. Possible values are:<br/> 1. **MAIL** (for transactions where the payment details are captured manually and provided in written form the Card Code entry is not allowed)<br/> 2. **PHONE** (for transactions where you have received the order over the phone and enter the payment details yourself the Card Code entry is required)<br/> 3. **ECI** (for standard usage in an eCommerce environment)|
|vattax|This field allows you to submit an amount for Value Added Tax or other taxes, e.g. GST in Australia. Please ensure the sub total amount plus shipping plus tax equals the charge total.|

### HTML Form Fields for Specific Functionalities

Some functionalities create the need additional fields or fields that become mandatory which would otherwise be optional, either for the addendum to be achieved, scheme requirements met for specific MCCs or to send required information for a specific payment method, as below:

> - Purchasing Cards Level II and Level III

> - MCC6012 Mandate in the UK

> - DCC and Installment Card Related

> - SEPA Direct Debit

> - MasterPass

> - China Domestic Payments

[Click here to view the HTML fields relevant to these.](?path=docs/additionalInfo/HTMLFormFieldsSpecific.md) 

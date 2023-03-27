
# Optional HTML Form Fields


If you post a HTML form to initiate the payment, there are a number of optional fields that you can include in your request for different purpose.

### Checkout Experience Related Fields

| *Field*: | *Comment*|
|----|----|
| hideOrderDetails | Set this parameter to ‘true’ when you want to remove the Your Order box from our hosted page in the checkout option ‘combinedpage’. |
|idealIssuerID |This parameter can be used to submit the iDEAL issuing bank in case you let your customers select the issuer within your shop environment. If you do not pass this value for an iDEAL transaction, a hosted selection form will be displayed to your customer, from Table below  **TABLE1**|
|language|This parameter can be used to override the default payment page language configured for your merchant store. The following values are currently possible, from below **TABLE2**|
| parentUri | If you plan to embed our hosted payment pages inside an iFrame you must use this parameter, with the maximum length of 2048 characters, to specify an URL of a page, where the hosted payment page will be embedded. However, note that we do not recommend using the hosted payment forms inside an iFrame since some Internet browsers do not allow cookies to be sent to the 3rd party hosts, moreover some features (e.g.: 3D Secure authentications) and some Alternative Payment methods that involve redirections to the 3rd party services (e.g.: iDEAL or PayPal) do not allow displaying their screens within an iFrame. |
| paymentMethod | If you let the customer select the payment method (e. g. MasterCard, Visa, Direct Debit) in your shop environment or want to define the payment type yourself, transmit the parameter ‘paymentMethod’ along with your Sale or PreAuth transaction. If you do not submit this parameter, the payment gateway will display a drop-down menu to the customer to choose from the payment methods available for your shop. [See valid values here](?path=docs/additionalInfo/OtherOptionalFields.md)|
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


### Consumer Information

### Card Related Fields

### Additional Transaction Information

### HTML Form Fields for Specific Functionalities

[Click here to view the HTML fields relevant to these.]


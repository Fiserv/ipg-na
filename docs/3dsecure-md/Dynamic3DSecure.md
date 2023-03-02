
# Dynamic 3-D Secure

With the Dynamic 3-D Secure product option you can exclude specific card transactions from the 3-D Secure authentication based on a certain country selection (i.e.: issuing country) while applying the standard 3-D Secure authentication process for other transactions with card from other countries. 

You can improve the consumer experience for the cardholders from the selected countries, while the chargeback risk for such transactions is still with you.

If you have ordered this product option, the countries that should be excluded from the 3-D Secure authentication process can be set up for you by your local support team.

In case of specific high-risk transactions, you can override this setting on transaction level and force the 3-D Secure authentication on a Transaction-by-Transaction basis, even if the card used is issued in a country that has been defined by you as a country where 3-D Secure authentication should not be applied. In order to do this, you have to send the parameter ‘override3dsCountryExclusion’ set to “true”. The country setting will then be ignored and the 3-D Secure authentication process applied.

|*Field Name*|*Description, possible values and format*|
|----|----|
|override3dsCountryExclusion|Optional parameter to be set either to ‘true’ or ‘false’. <br/> Set to ‘true’ if for a transaction you would like to enforce 3-D Secure authentication, despite this country possibly being exempted from authentication due to the merchant configured list of countries, where 3-D Secure is not required.

> [Back to 3-D Secure main page](?path=docs/3dsecure-md/3DSecure.md)| 
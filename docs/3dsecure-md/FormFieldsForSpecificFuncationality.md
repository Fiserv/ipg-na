
# HTML Form Fields for Specific Functionalities

Some functionalities create the need additional fields or fields that become mandatory which would otherwise be optional, either for the addendum to be achieved, scheme requirements met for specific MCCs or to send required information for a specific payment method, as below:

- 3-D Secure

- Credential-on-file transactions

- Purchasing Cards Level II and Level III

- MCC6012 Mandate in the UK

- DCC and Installment Card Related 

- Sepa Direct Debit

- China Domestic Payments

- Korea Domestic Payments 

## 3-D Secure

|*Field *|*Comment*|
|----|----|
|authenticateTransaction|Optional parameter to be set either to ‘true’ or ‘false’ to enable or disable 3-D Secure authentication on a Transaction-by-Transaction basis.<br/> Example for a transaction with 3-D Secure:<br/><input type="hidden" name="authenticateTransaction" value="true"/> <br/> Example for a transaction without 3D Secure: <br/><input type="hidden" name="authenticateTransaction" value="false"/>|
|threeDSRequestorChallengeIndicator|Optional parameter for EMV 3-D Secure (2.0) to be set to: 01,02,03,04 in order to indicate the preferred type of authentication:<br/> 01 - no preference (set as default value) <br/>02 - no challenge requested <br/>03 - challenge requested (3DS requestor preference)<br/>04 - challenge requested (mandate)|
|threeDSTransType|The parameter for EMV 3-D Secure (2.0), represents the type of purchased item, mandatory for Visa and Brazilian market, otherwise optional. If no specific value present in the transaction request, default value is used.<br/>01 - Goods/ Service Purchase (default value)<br/>03 - Check Acceptance<br/>10 - Account Funding<br/>11 - Quasi-Cash Transaction<br/>28 - Prepaid Activation and Load|
|scaExemptionIndicator1|Use this optional parameter to request an exemption from Strong Customer Authentication (SCA) without the need to perform 3-D Secure authentication. Currently available values: <br/>Low Value Exemption<br/>TRA Exemption<br/>Trusted Merchant Exemption<br/>SCP Exemption<br/>Note: please be aware, that this parameter is relevant only for the distribution channels impacted by PSD2 requirements|
|skipTRA|This optional parameter allows you to use 3D Secure even if the transaction has been evaluated as low risk and would be eligible for an exemption. Currently available values: <br/> true <br/>false<br/>When your store has been set up with Transaction Risk Analysis (TRA) service, but you do want to force 3D Secure authentication for a certain transaction, set ‘skipTRA’ to ‘true’.<br/>Note this parameter is relevant only for the European merchants impacted by the PSD2 requirements.|
|oid|Use this optional parameter to assign an identifier for your order; in case you plan to authenticate the transaction using EMV 3DS protocol (aka 3DS 2.1) only the following characters are allowed:<br/> A-Z, a-z, 0-9, "-"|


## Credential-on-file Transactions

## Purchasing Cards - Level II Data

## Purchasing Cards - Level III Data (line item details in JSON format)

## MCC 6012 Mandate in the UK

An MCC, or merchant category code, is a four-digit number assigned to a business by card companies. It is used to classify businesses by their goods or service offerings. In this particular instance, the merchant category code 6012 is for businesses who are classified as Financial Institutions.

For UK-based Financial Institutions with Merchant Category Code 6012, Visa and MasterCard have mandated additional information of the primary recipient of the loan to be included in the authorization message.

As per this mandate, you must use the following parameters for your transaction requests:

## Card Related Fields

## Information Required For Specific Payment Methods

**SEPA Direct Debit**

**China Domestic Payments**

**Korea Domestic Payments**



# HTML Form Fields for Specific Functionalities


Some functionalities create the need additional fields or fields that become mandatory which would otherwise be optional, either for the addendum to be achieved, scheme requirements met for specific MCCs or to send required information for a specific payment method, as below:

> - 3-D Secure

> - Credential-on-file transactions

> - Purchasing Cards Level II and Level III

> - MCC6012 Mandate in the UK

> - DCC and Installment Card Related 

> - Sepa Direct Debit

> - China Domestic Payments

> - Korea Domestic Payments

## 3-D Secure

| *Field*: | *Comment*|
|----|----|
|authenticateTransaction|Optional parameter to be set either to ‘true’ or ‘false’ to enable or disable 3-D Secure authentication on a Transaction-by-Transaction basis.<br/>Example for a transaction with 3-D Secure:<br/> ``` <input type="hidden" name="authenticateTransaction" value="true"/> ``` <br/>Example for a transaction without 3D Secure:<br/> ``` <input type="hidden" name="authenticateTransaction" value="false"/> ```|
|threeDSRequestorChallengeIndicator|Optional parameter for EMV 3-D Secure (2.0) to be set to: 01,02,03,04 in order to indicate the preferred type of authentication:<br/><br/>01 - no preference (set as default value)<br/>02 - no challenge requested <br/>03 - challenge requested (3DS requestor preference)<br/>04 - challenge requested (mandate)|
|threeDSTransType|The parameter for EMV 3-D Secure (2.0), represents the type of purchased item, mandatory for Visa and Brazilian market, otherwise optional. If no specific value present in the transaction request, default value is used.<br/><br/>01 - Goods/ Service Purchase (default value)<br/>03 - Check Acceptance <br/>10 - Account Funding <br/>11 - Quasi-Cash Transaction <br/>28 - Prepaid Activation and Load|
|scaExemptionIndicator1|Use this optional parameter to request an exemption from Strong Customer Authentication (SCA) without the need to perform 3-D Secure authentication. Currently available values:<br/><br/> 1. Low Value Exemption<br/> 2. TRA Exemption<br/> 3. Trusted Merchant Exemption<br/> 4. SCP Exemption<br/>Note: please be aware, that this parameter is relevant only for the distribution channels impacted by PSD2 requirements|
|skipTRA|This optional parameter allows you to use 3D Secure even if the transaction has been evaluated as low risk and would be eligible for an exemption. Currently available values:<br/><br/> - true<br/> - false<br/><br/>When your store has been set up with Transaction Risk Analysis (TRA) service, but you do want to force 3D Secure authentication for a certain transaction, set ‘skipTRA’ to ‘true’.<br/>Note this parameter is relevant only for the European merchants impacted by the PSD2 requirements.|
|oid|Use this optional parameter to assign an identifier for your order; in case you plan to authenticate the transaction using EMV 3DS protocol (aka 3DS 2.1) only the following characters are allowed: <br/><br/> **A-Z, a-z, 0-9, "-"**|

## Credential-on-file Transactions

| *Field*: | *Comment*|
|----|----|
|unscheduledCredentialOnFileType|This field allows you to flag transactions as unscheduled credential on file type. Currently the valid values are: FIRST, CARDHOLDER_INITIATED or MERCHANT_INITIATED to advise the type of transaction for these scenarios|
|referencedSchemeTransactionId|This field allows you to include the payment scheme's transaction ID that has been returned in the response of the initial transaction (when credentials have been stored) in order to provide a reference to that original transaction|

## Purchasing Cards - Level II Data

| *Field*: | *Comment*|
|----|----|
|pcCustomerReferenceID|Merchant-defined reference for the customer that will appear on the customer’s statement.|
|pcSupplierInvoiceNumber|Merchant-defined reference for the invoice – invoice number.|
|pcSupplierVATRegistrationNumber|The ID number assigned by the tax authorities to the merchant.|
|pcTotalDiscountAmount|Total discount applied to a transaction (i.e. total transaction percentage discounts, fixed transaction amount reductions or summarization of line item discounts).|
|pcTotalDiscountRate|Rate of discount for the whole transaction.|
|pcVATShippingRate|Total shipping amount applied to the transaction. Merchants can choose to deliver contents of a single transaction in multiple shipments and this field reflects the total cost of those deliveries|
|pcVATShippingAmount|Total shipping amount applied to the transaction. Merchants can choose to deliver contents of a single transaction in multiple shipments and this field reflects the total cost of those deliveries|
|pcLineItemsJson|Line item details in JSON format. See table below.|

## Purchasing Cards - Level III Data (line item details in JSON format)

| *Field*: | *Comment*|
|----|----|
|CommodityCode|Reference to a commodity code used to classify a purchased item.|
|ProductCode|Reference to a merchant product identifier – Universal Product Code (UPC) of a purchased item.|
|Description|Description of purchased item.|
|Quantity|Quantity of purchased items.|
|UnitOfMeasure|Unit of measure of purchased items.|
|UnitPrice| Mandatory data for Level III transactions.|
|VATAmountAndRate|Rate of the VAT amount e.g. 0.09 = 9%|
|DiscountAmountAndRate|Rate of the discounted amount e.g. 0.09 = 9%|
|LineItemTotal|Calculation of the unit cost multiplied by the quantity and less the discount per line item.<br/>[Unit Cost * Quantity] – Discount per Line Item = Line Item Total.|




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

|*Field*|*Comment*|
|----|----|
|authenticateTransaction|Optional parameter to be set either to ***true*** or ***false*** to enable or disable 3-D Secure authentication on a Transaction-by-Transaction basis.<br/> Example for a transaction with 3-D Secure:<br/><input type="hidden" name="authenticateTransaction" value="true"/> <br/> Example for a transaction without 3D Secure: <br/><input type="hidden" name="authenticateTransaction" value="false"/>|
|threeDSRequestorChallengeIndicator|Optional parameter for EMV 3-D Secure (2.0) to be set to: 01,02,03,04 in order to indicate the preferred type of authentication:<br/> 01 - no preference (set as default value) <br/>02 - no challenge requested <br/>03 - challenge requested (3DS requestor preference)<br/>04 - challenge requested (mandate)|
|threeDSTransType|The parameter for EMV 3-D Secure (2.0), represents the type of purchased item, mandatory for Visa and Brazilian market, otherwise optional. If no specific value present in the transaction request, default value is used.<br/>01 - Goods/ Service Purchase (default value)<br/>03 - Check Acceptance<br/>10 - Account Funding<br/>11 - Quasi-Cash Transaction<br/>28 - Prepaid Activation and Load|
|scaExemptionIndicator1|Use this optional parameter to request an exemption from Strong Customer Authentication (SCA) without the need to perform 3-D Secure authentication. Currently available values: <br/>Low Value Exemption<br/>TRA Exemption<br/>Trusted Merchant Exemption<br/>SCP Exemption<br/>Note: please be aware, that this parameter is relevant only for the distribution channels impacted by PSD2 requirements|
|skipTRA|This optional parameter allows you to use 3D Secure even if the transaction has been evaluated as low risk and would be eligible for an exemption. Currently available values: <br/> true <br/>false<br/>When your store has been set up with Transaction Risk Analysis (TRA) service, but you do want to force 3D Secure authentication for a certain transaction, set ***skipTRA*** to ***true***.<br/>Note this parameter is relevant only for the European merchants impacted by the PSD2 requirements.|
|oid|Use this optional parameter to assign an identifier for your order; in case you plan to authenticate the transaction using EMV 3DS protocol (aka 3DS 2.1) only the following characters are allowed:<br/> A-Z, a-z, 0-9, "-"|


## Credential-on-file Transactions

|*Field*|*Comment*|
|----|----|
|unscheduledCredentialOnFileType|This field allows you to flag transactions as unscheduled credential on file type. <br/> Currently the valid values are: FIRST, CARDHOLDER_INITIATED or MERCHANT_INITIATED to advise the type of transaction for these scenarios|
|referencedSchemeTransactionId|This field allows you to include the payment scheme**s transaction ID that has been returned in the response of the initial transaction (when credentials have been stored) in order to provide a reference to that original transaction|


## Purchasing Cards - Level II Data

|*Field*|*Comment*|
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

|*Field*|*Comment*|
|----|----|
|CommodityCode|Reference to a commodity code used to classify a purchased item.|
|ProductCode|Reference to a merchant product identifier – Universal Product Code (UPC) of a purchased item.|
|Description|Description of purchased item.|
|Quantity|Quantity of purchased items.|
|UnitOfMeasure|Unit of measure of purchased items.|
|UnitPrice|Mandatory data for Level III transactions.|
|VATAmountAndRate|Rate of the VAT amount e.g. 0.09 = 9%|
|DiscountAmountAndRate|Rate of the discounted amount e.g. 0.09 = 9%|
|LineItemTotal|Calculation of the unit cost multiplied by the quantity and less the discount per line item.<br/> [Unit Cost * Quantity] – Discount per Line Item = Line Item Total.|


## MCC 6012 Mandate in the UK

An MCC, or merchant category code, is a four-digit number assigned to a business by card companies. It is used to classify businesses by their goods or service offerings. In this particular instance, the merchant category code 6012 is for businesses who are classified as Financial Institutions.

For UK-based Financial Institutions with Merchant Category Code 6012, Visa and MasterCard have mandated additional information of the primary recipient of the loan to be included in the authorization message.

As per this mandate, you must use the following parameters for your transaction requests:

|*Field*|*Comment*|
|----|----|
|mcc6012BirthDay|Recipient date of birth in format: dd.mm.yyy|
|mcc6012AccountFirst6|First 6 digits of recipient PAN (where the primary recipient account is a card|
|mcc6012AccountLast4|Last 4 digits of recipient PAN (where the primary recipient account is not a card|
|mcc6012AccountNumber|Recipient account number (where the primary recipient account is not a card|
|mcc6012Surname|Surname|
|mcc6012Zip|Post Code|

## Card Related Fields

|*Field*|*Comment*|
|----|----|
|dccInquiryId|Inquiry ID for a Dynamic Pricing request. Used to send the Inquiry ID you have obtained via an API call. This value will be used to retrieve the currency conversion information (exchange rate, converted amount) for this transaction|
|numberOfInstallments|This parameter allows you to set the number of instalments for a Sale transaction if your customer pays the amount in several parts|
|installmentsInterest|This parameter allows you to choose, if instalment interest should be applied or not, the values “true” or “false” are currently possible|
|installmentDelayMonths|This parameter allows you to delay the first instalment payment for several months, values 2-99 are currently possible|


## Information Required For Specific Payment Methods

**SEPA Direct Debit**

|*Field*|*Comment*|
|----|----|
|bname|Name of bank account owne|
|baddr1|Mandatory if IBAN belongs to EFTA and associated country. Street name and house number of the bank account owner that will be debited (alphanumeric characters, spaces, and dashes limited to 96 characters)|
|bcity|Mandatory if IBAN belongs to EFTA and associated country. City of the bank account owner that will be debited (alphanumeric characters, spaces, and dashes limited to 96 characters)|
|bcountry|Mandatory if IBAN belongs to EFTA and associated country. Country of the bank account owner that will be debited (2 letter country code|
|bzip|Mandatory if IBAN belongs to EFTA and associated country. Zip or postal code of the bank account owner that will be debited (limit of 24 characters incl. spaces|
|iban|International bank account number (up to 34 digits|
|mandateDate|This field allows you to reference to the date of the original mandate when performing recurring Direct Debit transactions. The date needs to be submitted in format YYYYMMDD. Please note that this is a mandatory field for recurring Direct Debit transactions.|
|mandateReference|This field allows you to transmit a Mandate Reference for Direct Debit payments. Please note the regulatory requisite to keep the Mandate Reference unambiguous|
|mandateType|This field allows you to process Direct Debit transactions that are based on mandates for recurring collections. The mandate type can be set to ‘single’ for single (one-off) debit collections, to ‘firstCollection’ when submitting the initial transaction related to a mandate for recurring Direct Debit collections, to ‘recurringCollection’ for subsequent recurring transactions or to ‘finalCollection’ for the last direct debit in a series of recurring direct debits. Transactions where this parameter is not submitted by the merchant will be flagged as a single debit collection. <br/> Please note that it is mandatory to submit a mandateReference in case of recurring collections.|
|mandateUrl|When your store is enabled for SEPA Direct Debit as part of the Local Payments offering, this field allows you to transmit a valid URL of SEPA Direct Debit mandate to enable the Risk and Compliance department to access the details. <br/> Please note that it is mandatory to submit a mandateReference and a mandateDate together with a mandateUrl in case you manage SEPA Direct Debit mandates on your side in the combination with the Fiserv Local Payments offering.|


**China Domestic Payments**

|*Field*|*Comment*|
|----|----|
|item1|Submit exactly one line item parameter with four (4) property values in the following format: id;description;quantity;item_total_price <br/> Transaction request without a line item or with multiple line items will be declined.<br/> *Example: 100018;The Hobbit;1;3.50* <br/> ***item1 Position,Property and Description see the table below***|
|customerid|Unique reference to identify the consumer|
|custom_domesticBankId|Submit a bank identifier for reporting purpose in relation to promotions with local Chinese banks. Max length 8.|
|customerid|Unique reference to identify the consumer|
|custom_domesticBankId|Submit a bank identifier for reporting purpose in relation to promotions with local Chinese banks. Max length 8.|


item1: Position,Property and Description:

|*Position*|*Property*|*Description*|
|----|----|----|
|1|id|Product code (编码Code) <br/> > [See valid values here](?path=docs/3dsecure-md/ChainaDomesticProductCatalog.md) |
|2|description|Product name|
|3|quantity|Quantity of product(s)|
|4|item_total_price|Price of product(s)|

**Korea Domestic Payments**

|*Field*|*Comment*|
|----|----|
|checkoutoption|Set this parameter to ***combinedpage*** for Korea domestic payments|
|oid|Unique order ID, alphanumeric string (32 max)|
|mobileMode|Set the value for this parameter to ‘true’. This will lead your customer to a payment page flow that has been specifically designed for mobile devices.|
|numberOfInstallments|Optional parameter to set the installment options that will be offered for that transaction.<br/> Possible values are:<br/> **00**: lumpsum (No Installments)<br/>**02**~**60**: 2 months ~60 months<br/>Otherwise by default: 0~ 12 months (If installment is configured)<br/> You need to be configured for installments during boarding.|
|localTax|Optional parameter to submit an amount for Local Tax. Please ensure the sub total amount plus local tax equals the charge total.|
|subTotal|Optional parameter to submit a tax free amount. Please ensure the sub total amount plus local tax equals the charge total.|
|customParam_kps_ItemInfo|Type of purchased item, alphanumeric string (1 max)<br/> Possible values are:<br/> **1**: Goods<br/>**2**: Online content|
|customParam_kps_CcProdDesc|Description of purchased items to be displayed on the KPS payment page, alphanumeric string (256 max)|
|customParam_kps_VAExpireDate|The Effective/Valid Time for Virtual Bank Acct. Optionally required for Virtual Account payment method.<br/> Format: YYYYMMDDHH24MISS|
|customParam_kps_SelectPayment|Optional parameter to restrict available payment methods for a transaction.<br/>Possible values are:<br/>**ALL**: All (Default)<br/>**CRDT**: Card<br/> **HP**: Mobile carrier billing<br/> **ACCT**: Bank account transfer <br/>**VACT**: Virtual bank account transfer <br/>**IC**: CashCard<br/> **SPAY**: e-Wallet (e.g.: Samsung Pay, 11Pay, Payco)|
|customParam_kps_LangType|Optional parameter to choose the Payment Page Display Language.<br/>Possible values are:<br/> **HAN**: Korean (Default)<br/> **ENG**: English|
|customParam_kps_BillType|Optional parameter to choose the Billing Type for the transaction.<br/>Possible values are:<br/>**00**: Taxable (Default)<br/>**01**: Duty free|
|customParam_kps_CardSelect|Optional parameter to restrict available issuers for a transaction. All issuers are available if this parameter is not set.<br/>Possible values are:<br/>**00** - All Issuers<br/>**01** - BC<br/>**07** - KB<br/>**02** - Shinhan<br/>**03** - Samsung<br/>**05** - Lotte<br/>**12** - NH<br/>**27** - Hana<br/>**04** - Hyundai<br/>**13** - CITI<br/>**22** - Jeju<br/>**14** - Woori<br/>**11** - Suhyup<br/>**24** - Jeonbok<br/>**23** - Kwangju<br/>**17** - Shinhyup<br/>**09** - All of International Issuers|
|customParam_kps_escrowYn|Optional parameter to manage ESCROW options. Applicable only for Bank Account Transfer and Virtual Bank Account Transfer Payment methods.<br/>Possible values are:<br/>**S**: Customer can choose to use ESCROW (Default)<br/>**Y**: ESCROW is required regardless of customers choice <br/> **N**: Customer cannot user ESCROW<br/>Escrow is a legal arrangement in which a third party temporarily holds large sums of money or property until a particular condition has been met (such as the fulfillment of a purchase agreement).|
|customParam_kps_VAPhoneNumber|Optional parameter to receive SMS related to Virtual Account. If not set, Customer has the option to enter it in the payment screen. Applicable only for Virtual Account.|
|customParam_kps_FXFlag|Foreign exchange payment flag.<br/> This parameter in mandatory only when the transaction must happen in any currency other than KRW. If the transaction should happen in KRW, then don’t use this parameter.|
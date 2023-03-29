
# Response Details

Upon completion, the transaction details will be sent back to the defined URL as hidden fields:


| *Field Name*:   | *Description*|
|----|----|
|approval_code | Approval code for the transaction. The first character of this parameter is the most helpful indicator for verification of the transaction result.<br/>‘Y’ indicates that the transaction has been successful<br/>‘N’ indicates that the transaction has not been successful<br/>“?” indicates that the transaction has been successfully initialized, but a final result is not yet available since the transaction is now in a waiting status. The transaction status will be updated at a later stage.|
|oid|Order ID|
|refnumber|Reference number|
|status|Transaction status, e.g. ‘APPROVED’, ‘DECLINED’ (by authorisation endpoint or due to fraud prevention settings),‘FAILED’ (wrong transaction message content/parameters, etc.) or ‘WAITING’ (asynchronous Alternative Payment Methods)|
|txndate_processed|Time of transaction processing|
|ipgTransactionId|Transaction identifier assigned by the gateway, e.g. to be used for a Void|
|tdate|Identification for the specific transaction|
|fail_reason|Reason the transaction failed|
|response_hash|Hash-Value to protect the communication (see a note here)|
|processor_response_code |The response code provided by the backend system.<br/>Please note that response codes can be different depending on the used payment type and backend system. While for credit card payments, the response code ‘00’ is the most common response for an approval, the backend for giropay transactions for example returns the response code ‘4000’ for succesful transactions.|
|fail_rc|Internal processing code for failed transactions|
|terminal_id|Terminal ID used for transaction processing|
|ccbin|6 digit identifier of the card issuing bank|
|cccountry|3 letter alphanumeric ISO code of the cardholder’s country (e.g. USA, DEU, ITA, etc.)<br/>Filled with “N/A” if the cardholder’s country cannot be determined or the payment type is not credit card|
|ccbrand|Brand of the credit or debit card:<br/>MASTERCARD<br/>VISA<br/>AMEX<br/>DINERSCLUB<br/>JCB<br/>CUP<br/>CABAL<br/>MAESTRO<br/>RUPAY<br/>BCMC<br/>SOROCRED<br/>Filled with “N/A” for any payment method which is not a credit card or debit card<br/>|

**For 3-D Secure transactions only:**

| *Field Name*:   | *Description*|
|----|----|
|response_code_3dsecure|Return code indicating the classification of the transaction:<br/><br/>1 – Successful authentication (VISA ECI 05, MasterCard ECI 02)<br/>2 – Successful authentication without AVV (VISA ECI 05, MasterCard ECI 02)<br/>3 – Authentication failed / incorrect password (transaction declined ECI 07)<br/>4 – Authentication attempt (VISA ECI 06, MasterCard ECI 01)<br/>5 – Unable to authenticate / Directory Server not responding (VISA ECI 07)<br/>6 – Unable to authenticate / Access Control Server not responding (VISA ECI 07)<br/>7 – Cardholder not enrolled for 3D Secure (VISA ECI 07)<br/>8 – Invalid 3D Secure values received, most likely by the credit card issuing bank’s Access Control Server (ACS)<br/>Please see note about blocking ECI 7 transactions in the 3-D Secure section of this document.|

**Credential-on-file transactions only:**

| *Field Name*:   | *Description*|
|----|----|
|schemeTransactionId     |Returned in the response by a scheme for stored credentials transactions to be used in subsequent transaction requests as a reference|

**For Currency Conversion transactions only:**

| *Field Name*:   | *Description*|
|----|----|
|dcc_foreign_amount	|Converted amount in cardholder home currency. Decimal number with dot (.) as a decimal separator|
|dcc_foreign_currency |ISO numeric code of the cardholder home currency. This transaction is performed in this currency.|
|dcc_margin_rate_percentage |Percent of margin applied to the original amount. Decimal number with dot (.) as a decimal separator.|
|dcc_rate_source	|Name of the exchange rate source (e.g. Reuters Wholesale Inter Bank)|
|dcc_rate	|Exchange rate. Decimal number with dot (.) as a decimal separator.|
|dcc_rate_source_timestamp	|Exchange rate origin time. Integer - Unix timestamp (seconds since 1.1.1970)|
|dcc_accepted	|Indicates if the card holder has accepted the conversion offer (response value ‘true’) or declined the offer (response value ‘false’).|

**For iDEAL transactions only:**

| *Field Name*:   | *Description*|
|----|----|
|accountOwnerName | Name of the owner of the bank account that has been used for the iDEAL transaction |
|iban|IBAN of the bank account that has been used for the iDEAL transaction|
|bic	|BIC of the bank account that has been used for the iDEAL transaction|

**For Fraud Detect transactions only:**

| *Field Name*:   | *Description*|
|----|----|
|fraudScore|Score returned based on Fraud Detect check|

**For SEPA Direct Debit as part of the TeleCash from Fiserv offering:**

| *Field Name*:   | *Description*|
|----|----|
|bname	|Name of the account holder of the bank account that has been used|
|bic	|BIC is provided only if the German IBAN has been used|
|iban	|IBAN of the bank account that has been used|
|mandateReference       |Mandate reference as returned for the first direct debit transaction|
|mandateDate|Date of the initial direct debit transaction as returned for the first transaction|

**For merchants using Global Merchant Acquiring model only:**

| *Field Name*:   | *Description*|
|----|----|
|associationResponseCode  |The raw association value tells exactly how the issuer has responded to the transaction without any mapping done either by the authorization platform or the gateway. It will be returned only for Visa, MasterCard, Amex, and Discover|

**When using your own error page for negative validity checks (full_bypass=true):**

| *Field Name*:   | *Description*|
|----|----|
|fail_reason_details |Comma separated list of missing or invalid variables.<br/>Note that ‘fail_reason_details’ will not be supported in case of payplus and fullpay mode.|
|invalid_cardholder_data|true – if validation of card holder data was negative<br/>false – if validation of card holder data was positive but transaction has been declined due to other reasons|
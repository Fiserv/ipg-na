
# Response Codes


**Address Verification Service (AVS) Results**

*The AVS response logic is the following:* <br/> **The 1st letter of the AVS code relates to the street address <br/> The 2nd letter of the AVS code relates to the postcode/zip whereas the letters indicate:**

| *Value*:   | *Meaning*|
|----|----|
| Y | The submitted value matches with the card issuer's records|
| N | The submitted value does not match with the card issuer's records|
| P | No value has been provided or the provided value has not been checked by the card issuer|

**Address Verification Service (AVS) Results**

| *Value*:   | *Meaning*|
|----|----|
| M | Card Security Code matches|
| N | Card Security Code does not match|
| P | Not processed|
| S | Merchant has indicated that the card security code is not present on the card|
| U | Issuer is not certified and/or has not provided encryption keys|
| X | No response from the credit card association was received. <br/> A blank response indicates that no code was sent and that there was no indication that the code was not present on the card.|

**Most Common Response Codes**

| *Authorization Response Code*   | *Response Code Description*| *Gateway Approval Code Example* |
|----|----|----|
| 00 | Transaction has been approved.| Y:000000:3989951798:PPX:259280509 |
| 05 | The card being used for the transaction has been rejected by the issuer.|N:05:Do Not Honour |
| 5003 | The order is already existing in the database.	| N:-5003:The order already exists in the database. |
| 5005 | Cardholder submitted the transaction more than once during the 'duplicate lockout' window of time set. (eg: by pressing submit twice)	| N:-5005:FRAUD - Duplicate lockout |
| 5101 | 3D Secure authentication failed (eg: cardholder entered incorrect password) | N:-5101:3D Secure authentication failed |
| 5103 | Cardholder did not return from Access Control Server redirection.  (ACS - issuer component of 3D Secure)| N:-5103:Cardholder did not return from ACS |
| 5993 | The transaction has been cancelled by the consumer.| N:-5993:Cancelled by user |
| 12000 | The merchant has the service entry Card Code Mandatory, but sent a transaction without card code value. | N:-12000:Card security code is mandatory |

*For a list of response codes specific to your authorisation platform please check:*  [AuthorisationPlatform](?path=docs/schemas-md/AuthorisationPlatform.md)


**Response Codes Related to Configuration Issues**

| *Authorization Response Code*   | *Response Code Description*| *Gateway Approval Code* |
|----|----|----|
| 5002 | The merchant does not have a service entry for the card brand that has been used in the transaction request. | N:-5002:brand not supported |
| 30053 | The transaction timed out | N:-30053:Communication Error |
| 30053 | Exception occurred retrieving the message from the endpoint.| N:-30053:Communication Error |
| 30060 | An error occurred building, parsing or interpreting the message. | N:30060:Internal Error |
| 50653 | Incorrect currency has been sent in the request. | N:-50653:Sent invalid currency or no currencies were setup for this store |

**Response Codes Related to Configuration Issues**

| *Authorization Response Code*   | *Response Code Description*| *Gateway Approval Code* |
|----|----|----|
| PP00001 |Cardholder did not return from local payment redirection. | N:-PP00001:Cardholder did not return from alternate payment |
| P00001 | Cardholder cancelled the payment. | N:-P00001:Cancelled by user |
| INPUT_DATA | Transaction input data are incorrect, channel tag or transaction has not been found.| N:INPUT_DATA:Invalid input data|
| QUOTA | Refund quota exceeded - not enough funds available. | N:QUOTA:APM|

*Authorisation Platform Specific Response Codes For a list of response codes specific to your authorisation platform please check:* [AuthorisationPlatform](?path=docs/schemas-md/AuthorisationPlatform.md)


# Billing/Shipping Information


If you post a HTML form to initiate the payment, you can include billing and shipping information in your request by using the following fields. Some of these fields are mandatory for specific alternative payment methods or relevant for fraud prevention purpose.

### Alternative Options

> [Billing information in API requests](?path=docs/schemas-md/Billing.md)

> [Shipping information in API requests](?path=docs/schemas-md/Shipping.md)

## Billing Information

| *Field*: | *Comment*|
|----|----|
| bcompany | Customer's company name. Alphanumeric characters, spaces and dashes limited to 96.|
| bname | Customer's name. Alphanumeric characters, spaces and dashes limited to 96.|
| baddr1 | Customer's billing address 1. Limit of 96 characters including spaces.| 
| baddr2 | Customer's billing address 2. Limit of 96 characters including spaces.| 
| bcity | Billing City. Limit of 96 characters including spaces.| 
| bstate | State, Province or Territory. Limit of 96 characters including spaces.| 
| bcountry | Country of Billing Address. Two letter country code.| 
| bzip | Zip or Postal Code. Limit of 24 characters including spaces.| 
| phone | Customer's Phone Number. Limit of 32 characters.| 
| fax |	Customer's Fax Number. Limit of 32 characters.| 
| email | Customer's Email Address. Limit of 254 characters.|

## Shipping Information

| *Field*: | *Comment*|
|----|----|
|sname|	Ship-to name. Alphanumeric characters, spaces and dashes limited to 96.|
|saddr1|Shipping Address Line 1. Limit of 96 characters including spaces.|
|saddr2|Shipping Address Line 2. Limit of 96 characters including spaces.|
|scity|	Shipping City. Limit of 96 characters including spaces.|
|sstate|State, Province or Territory. Limit of 96 characters including spaces.|
|scountry| Country of Billing Address. Two letter country code.|
|szip| Zip or Postal Code. Limit of 24 characters including spaces.|

# 3-D Secure

3-D Secure is a messaging protocol developed by EMVCo to support app-based authentication and integration with digital wallets, as well as traditional browser based eCommerce transactions. The solution introduces many benefits to the marketplace as they will reflect the payment communities objective to secure consumer eCommerce transactions while optimizing the user experience.

If your merchant account is enabled for 3-D Secure, all sale or preauth transactions that you initiate by posting an HTML form will by default go through the 3-D Secure process without the need for you to do anything, i.e. cardholders with an enrolled card will see a page from the card issuer to enter the password unless the card issuer decides not to check it.

After the authentication, we bring the cardholder back to your webstore. If your credit card agreement includes 3-D Secure and your Merchant ID has been activated to use this service, you do not need to modify your payment page.

The following represents an example of a ***Sale*** transaction request with minimum set of fields including optional ***Challenge Indicator*** element:

```{r}

<!-- #include file=ipg-util.asp-->
<html>
<head><title>IPG Connect Sample for ASP</title></head>
<body>
<p><h1>Order Form</h1></p>
<form method=post action= https://test.ipg-online.com/connect/gateway/processing >
    <input type=hidden name=txntype value=sale>
    <input type=hidden name=checkoutoption value=combinedpage>
    <input type=hidden name=timezone value=Europe/Berlin/>
    <input type=hidden name=txndatetime value=<% getDateTime() %>/>
    <input type=hidden name=hash_algorithm value=HMACSHA256/>
    <input type=hidden name=hashExtended value=<% call createExtendedHash( 13.00,978 ) %>/>
    <input type=hidden name=storename value=110995000 />
    <input type=hidden name=mode value=payonly/>
    <input type=hidden name=paymentMethod value=V/>
    <input type=text name=chargetotal value=13.00 />
    <input type=hidden name=currency value=978/>
    <input type=hidden name=authenticateTransaction value=true/>
    <input type=text name=threeDSRequestorChallengeIndicator value=�1�/>
    <input type=submit value=Submit>
</form>
</body>
</html>

```

**NOTE**: *In case you submitted OrderId element in your request, please make sure to include only allowed characters: A-Z, a-z, 0-9, -*

The result of the transaction will be sent back to the defined ***responseSuccessURL*** or ***responseFailURL*** as hidden fields:

```{r}

{txndate_processed=20/04/10 13:37:33, 
ccbin=542606, 
timezone=CET, 
oid=C-2101f68a-45e9-4f3c-a6da-1337d5574717, 
cccountry=N/A, 
expmonth=12, 
currency=978, 
chargetotal=13.99, 
approval_code=Y:ECI2/5:Authenticated, 
hiddenSharedsecret=sharedsecret, 
hiddenTxndatetime=2019:04:10-13:37:08, 
expyear=2024, 
response_hashExtended=927d3c3108d596c593f74fd79184ece7c33103fe, 
response_code_3dsecure=1, 
hiddenStorename=12345678, 
transactionNotificationURL=https://test.ipg-online.com/webshop/transactionNotification, 
tdate=1554903428, 
ignore_refreshTime=on, 
ccbrand=VISA, 
txntype=sale, 
paymentMethod=V, 
txndatetime=2020:04:10-13:37:08, 
cardnumber=(VISA) ... 4979, 
ipgTransactionId=84120276797, 
status=APPROVED}

```

**Challenge indicator available values for 3DS protocol version 2.1 are:**

01 = No preference (You have no preference whether a challenge should be performed. This is the default value)
02 = No challenge requested (You prefer that no challenge should be performed.)
03 = Challenge requested: 3DS Requestor Preference (You prefer that a challenge should be performed)
04 = Challenge requested: Mandate (There are local or regional mandates that mean that a challenge must be   performed)

In case you have not used billing and shipping details in your authentication request before, please consider to include them to lower the 3-D Secure authentication declines.

## 3-D Secure Information in the Transaction Response

Upon completion, the transaction details will be sent back to the defined responseSuccessURL or responseFailURL as hidden fields.

Return code indicating the classification of the transaction:

1. Successful authentication (VISA ECI 05, MasterCard ECI 02)
2. Successful authentication without AVV (VISA ECI 05, MasterCard ECI 02)
3. Authentication failed / incorrect password / authentication rejected by the DS or ACS (transaction declined by the Gateway)
4. Authentication attempt (VISA ECI 06, MasterCard ECI 01)
5. Unable to authenticate / DS not responding (VISA ECI 07) - relevant for 3DS 1.0
6. Unable to authenticate / ACS or DS not responding (VISA ECI 07)
7. Cardholder not enrolled for 3-D Secure (VISA ECI 07) - relevant for 3DS 1.0
8. Invalid 3-D Secure values received 

|secure3D2AuthenticationResponse | secure3D2TransactionStatus | authenticationValue | ResponseCode3dSecure| 
|-------|--------|---------|----------|
|null	|null	|null	|null
|Y  |	null |	X |	1 |
|C  |	Y  |	X	|	1  |
|R  |	null  |	null  |	3  |
|R	  |	null  |	 X  | 3  |
|C  |	N  | null  |	3  |
|C  |	N  |	X  |	3  |
|A  |	null  |	X  |	4  |
|C  |	U  |	null  |	5  |
|U  |	null  |	null  |	5  |
|N  |	null  |	null  |	7  |	
|null  |	null  |	X  | 9  |
|Y  |	Y  |	X  |	1  |
|Y	  |	N  |	null  |		3  |
|Y  |	N  |	X  |	3  |
|Y  |	U  |	null  |	5  |

## Alternative Options

> [REST API Integration](?path=docs/3dsecure-md/RESTAPIIntegration.md)

> [SOAP API Integration](?path=docs/3dsecure-md/SOAPAPIIntegration.md)

> [Split Authentication and Authorization into two steps](?path=docs/3dsecure-md/3DSecureSplitAuthentication.md) 

## Enabling/Disabling 3-D Secure on a Transaction-by-Transaction Basis

The optional parameter authenticateTransaction can be used in case you want to send specific transactions without 3-D Secure.  

Check out how on our [Form Fields for Specific Functionalities](?path=docs/3dsecure-md/FormFieldsForSpecificFuncationality.md) page

## Dynamic 3-D Secure

With the Dynamic 3-D Secure product option you can exclude specific card transactions from the 3-D Secure authentication based on a certain country selection (i.e.: issuing country) e.g.: Germany, Switzerland and Austria, while applying the standard 3-D Secure authentication process for other transactions with card from other countries.

Check out our [Dynamic 3-D Secure](?path=docs/3dsecure-md/Dynamic3DSecure.md) page.

## Additional Information

- In principle, it may occur that 3-D Secure authentications cannot be processed successfully for technical reasons. If one of the systems involved in the authentication process is temporarily not responding, the payment transaction will be processed as a �regular� eCommerce transaction (ECI 7). A liability shift to the card issuer for possible chargebacks is not warranted in this case. If you prefer that such transactions shall not be processed at all, our technical support teams can block them for your Store on request.
 
- Credit card transactions with 3-D Secure hold in a pending status while cardholders search for their password or need to activate their card for 3-D Secure during their shopping experience. During this time when the final transaction result of the transaction is not yet determined, the payment gateway sets the Approval Code to �?:waiting 3dsecure�. If the session expires before the cardholder returns from the 3-D Secure dialogue with his bank, the transaction will be shown as �N:-5103:Cardholder did not return from ACS�.
 
- Please note that the technical process of 3-D Secure transactions differs in some points compared to a normal transaction flow. If you already have an existing shop integration and plan to activate 3-D Secure subsequently, we recommend performing some test transactions on our test environment, test data producing different authentication results can be found here: [3-D Secure Test Data](?path=docs/3dsecure-md/3DSecureTestData.md) 	
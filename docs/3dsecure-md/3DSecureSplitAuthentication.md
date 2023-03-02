
# 3-D Secure Split Authentication

If your business or technical processes require the cardholder authentication to be separated from the payment transaction (authorization), you can use the transaction type payer_auth. This transaction type only performs the authentication (and stores the authentication results).

## Example of a payer_auth Request

```{r}

<!-- #include file="ipg-util.asp"-->
<html>
<head><title>IPG Connect Sample for ASP</title></head>
<body>
<p><h1>Order Form</h1></p>
<form method="post" action=" https://test.ipg-online.com/connect/gateway/processing ">
    <input type="hidden" name="txntype" value="payer_auth">
                <input type="hidden" name="timezone" value="Europe/Berlin"/>
                <input type="hidden" name="txndatetime" value="<% getDateTime() %>"/>
                <input type="hidden" name="hash_algorithm" value="HMACSHA256"/>
                <input type="hidden" name="hashExtended" value="<% call createExtendedHash( "13.00","978" ) %>"/>
                <input type="hidden" name="storename" value="10123456789" />
    <input type="hidden" name="mode" value="payonly"/>
                <input type="hidden" name="paymentMethod" value="M"/>
    <input type="text" name="chargetotal" value="13.00" />
    <input type="hidden" name="currency" value="978"/>
                <input type="hidden" name="authenticateTransaction" value="true"/>
<input type="submit" value="Submit">
</form>
</body>
</html>

```

## Example of a payer_auth Response

```{r}

{txndate_processed=17/04/20 17:17:32, 
ccbin=542606, 
timezone=Europe/Berlin, 
oid=C-2101f68a-45e9-4f3c-a6da-1337d5574717, 
cccountry=N/A, 
expmonth=12, 
hash_algorithm=HMACSHA256
currency=978, 
chargetotal=13.00, 
approval_code=Y:ECI2/5:Authenticated, 
hiddenSharedsecret=sharedsecret, 
hiddenTxndatetime=2020:04:17-17:32:41, 
expyear=2024, 
response_hash=LarWYFSNgEToq13HlvyslX6hywi2T/nMn8jMY+1kxkI=,
response_code_3dsecure=1, 
hiddenStorename=10123456789, 
transactionNotificationURL=https://test.ipg-online.com/webshop/transactionNotification, 
tdate=1491824253, 
ignore_refreshTime=on, 
ccbrand=MASTERCARD, 
txntype=payer_auth, 
paymentMethod=M, 
txndatetime=2020:04:17-17:32:41, 
cardnumber=(MASTERCARD) ... 4979, 
**ipgTransactionId=84120276797**, 
status=APPROVED}

```

In a second step, you can then submit the payment transaction (sale or preauth) and reference to the prior authentication using the igpTransactionId from the payer_auth response.

 

> [Back to 3-D Secure main page](?path=docs/3dsecure-md/3DSecure.md)


# Transaction Response


## Step 2: Receiving the Transaction Result


### Response to Your Success and Failure URLs


When you have submitted your transaction request to our Gateway using a HTML form, the transaction result will be sent back to your Success and Failure URLs as hidden fields. You can define these URLs in the transaction request (see responseFailURL and responseSuccessURL parameters here). Alternatively you can define them once in the Customitzation section of our Virtual Terminal.

Please consider, when integrating, that new response parameters may be added from time to time in relation to product enhancements or new functionality.

Make sure to use the parameter 'response_hash' to recheck if the received transaction response has really been sent by Fiserv in order to protect you from fraudulent manipulations. The value is created with a HMAC Hash using the following parameter string:

approval_code|chargetotal|currency|txndatetime|storename
Shared secret ('sharedsecret') will be used as a key in HMAC to calculate the hash with the above hash string.

The hash algorithm is the same as the one that you have set in the transaction request. Please note that you have to store the 'txndatetime' in order to be able to calculate the hash.

### Server-to-Server Notifications

In addition to that mechanism, the Gateway can send server-to-server notifications to a defined URL. This is especially useful to keep your systems in synch with the status of a transaction for payment methods where the status can change at a later point. To use this notification method, you can specify an URL in the Customization section of the Virtual Terminal or submit the URL in the additional transaction parameter 'transactionNotificationURL'.

Please note that:

> - The Transaction URL is sent as received therefore please don't add additional escaping (e.g. using %2f for a Slash (/).
> - No SSL handshake, verification of SSL certificates will be done in this process.
> - The Notification URL needs to listen on port 443 (https) – other ports are not supported

The response hash parameter for validation (using the same algorithm that you have set in the transaction request) 'notification_hash' is calculated as follows:

**chargetotal|currency|txndatetime|storename|approval_code**

Shared secret ('sharedsecret') will be used as a key in HMAC to calculate the hash with the above hash string.

Such notifications can also be set up for the recurring payments that get automatically triggered by the gateway. Please contact your local support team to get a shared secret ('rcpSharedSecret') agreed for these notifications. You can configure your Recurring Transaction Notification URL ('rcpTransactionNotificationURL') in the Customisation section of the Virtual Terminal.

In case of recurring transactions the response hash parameter 'notification_hash' is calculated differently:

**chargetotal+rcpSharedSecret+currency+txndatetime+storename+approval_code**

The shared secret ('rcpSharedSecret') is part of the string (it is not used as a key in HMAC to calculate the hash with the hash string). Moreover, the response hash parameter for the recurring transaction notifications is calculated with the SHA256-value (as the default value).

### Response Details

> [Response Fields that will be sent to the defined URL](?path=docs/additionalInfo/ResponseDetails.md)

> [Response Codes](?path=docs/additionalInfo/ResponseCodes.md)

> [Authorisation Platform Specific Response Codes](?path=docs/additionalInfo/AuthorisationPlatformSpecificResponseCodes.md)

 
Next Steps
> Step 3: Completion When Goods Get Shipped
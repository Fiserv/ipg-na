
# How to generate a hash

If you are using an HTML form to initiate the sale or preauth transaction, your request needs to include a security hash for verification of the message integrity.

The Hash (parameter hashExtended) needs to be calculated using all non-empty gateway specified request parameters in ascending order of the parameter names, where the shared secret (parameter sharedsecret) must be used as the secret key for calculating the hash value. The gateway sorts the request parameters in the “natural order”. For strings this means the “Lexicographic Order", thus the upper-case characters come before the lower case (based on ASCII value).

The request parameters that are not specified in our solution can still be submitted in your request to the gateway, but they must be excluded from the hash calculation.  They will be ignored during processing and returned back in the response.  

When you are using Direct Post, there is also an option where you do not need to know the card details (PAN, CVV and Expiry Date) for the hash calculation. This will be managed with a specific setting performed on your store. Please contact your local support team if you want to enable this feature.

## Creating the hash with all parameters (hashExtended)

Transaction request values used for the hash calculation can be considered as a set of mandatory as well as optional gateway specified request parameters depending on the way you decide to build your request. See an example below:

> - chargetotal= 13.00
> - checkoutoption = combinedpage
> - currency= 978
> - hash_algorithm=HMACSHA256
> - paymentMethod=M
> - responseFailURL=https://localhost:8643/webshop/response_failure.jsp
> - responseSuccessURL=https://localhost:8643/webshop/response_success.jsp
> - storename=10123456789
> - timezone= Europe/Berlin
> - transactionNotificationURL=https://localhost:8643/webshop/transactionNotification
> - txndatetime=2021:09:06-16:43:04
> - txntype=sale
> - sharedsecret=sharedsecret (to be used as the secret key for calculating the hash value)

**Step 1.**  Extended hash needs to be calculated using all non-empty gateway specified request parameters in ascending order of the parameter names, where the upper-case characters come before the lower case (based on ASCII value). Join the parameters’ values to one string with pipe separator (use only parameters’ values and not the parameters’ names). 
```
stringToExtendedHash = 13.00|combinedpage|978|HMACSHA256|M|https://localhost:8643/webshop/response_failure.jsp|https://localhost:8643/webshop/response_success.jsp|10123456789|Europe/Berlin|https://localhost:8643/webshop/transactionNotification|2021:09:06-16:43:04|sale
```
The corresponding hash string does not include ‘sharedsecret’, which has to be used as the secret key for the HMAC instead.
The steps below provide the guidelines on how to calculate a hash, while using the values from our example.

**Step 2.** Pass the created string to the HMACSHA256 algorithm with the shared secret as a key for calculating the hash value.
```
HmacSHA256(stringToExtendedHash, sharedsecret)
```
**Step 3.** Encode the result of HMACSHA256 with Base64 and pass it to the gateway as part of your request.
```
Base64:
EapafBqqOF6N/kch8USkHPGh+fwSko24h6FpQnQHfQ8=
<input type="hidden" name="hashExtended" value="EapafBqqOF6N/kch8USkHPGh+fwSko24h6FpQnQHfQ8="/>
```
## Hash Generation Code Examples

> PHP
> ASP
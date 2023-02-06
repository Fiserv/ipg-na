
# Google Pay

Google Pay is the fast, simple way to pay in millions of places – online, in stores, and more. It brings together everything you need at checkout and keeps your information safe and secure.

**User Action**: the buyer taps the "Google Pay" button, and then selects a payment method and shipping address.

## If the purchase originates from a third-party site

	1. The merchant/client server issues a credential request with the Merchant ID and Processor Name as First Data to Google.
	2. Google returns response with encrypted payment credentials signed with the First Data key to the merchant server.
	3. The Merchant sends the encrypted payload to First Data.
	4. First Data decrypts and validates the payload, and then processes the transaction and responds back to merchant with either an approval or decline response.

## If the purchase originates from a Google site

	1. Google initiates a purchase request to the merchant after the consumer confirms order.
	2. The merchant/client server issues a request with the Merchant ID and Processor Name as First Data to Google.
	3. Google returns response with encrypted payment credentials signed with the First Data key to merchant server.
	4. The merchant sends the encrypted payload to First Data.
	5. First Data decrypts and validates the payload and process the transaction and respond back to merchant with either an approval or decline response.
 
 
To get more information on participating banks and countries for Google Pay, click here.


## Google Pay Integration

### Overview

Google Pay enables developers to add payment processing to merchants’ Android-compatible apps and on Chrome on Android. These APIs allow consumers to pay with any credit card they have stored in their Google account, including any cards they may have previously set up on their Android Pay digital wallet. Consumers may also add a new payment account.

The target audience for this document is a developer who wants to use Google Pay in their payment application.

 

### Merchant Boarding

Please reach out to your local Integration Support team for getting your account enabled.

### Prerequisites to build and run the sample Application  

Developers wishing to use the Fiserv Google Pay sample application will need the following software and hardware:

	 - Google Play Services version 18.0.0
	 - A physical device or an emulator to use for developing and testing. Google Play services can only be installed on an emulator with an AVD that runs Google APIs platform based on Android 4.4 or higher.
 	 - The latest version of Android Studio. This includes:
		o The latest version of the AndroidSDK, including the SDK Tools component. The SDK is available from the Android SDK Manager
	 - JavaJRE(JDKfordevelopment) as per Android SDK requirements.
Your project should be able to compile against Android 4.4 (KITKAT) or higher.

For more details, please refer "https://developers.google.com/pay/api/android/guides/setup"

### Changes to be made in the Application 

The following parameters need to be defined:

	a. Merchant ID
	b. Merchant Token
	c. APIKey
	d. APISecret

Define the Fiserv Object Parameters: Parameters must be updated in the following files: 

	 - Constants.java
	 - EnvData.java

Update the Constants.java file with the Merchant ID and Gateway Tokenization parameters. Note that:

	 - The Merchant ID will be shared by the Integration team and
	 - The Gateway Tokenization parameter defaults to ‘firstdata’. 

In the EnvData.java file, set the following environment variables, which will be shared by the Integration Team:

	 - APIKey –
	 - Token – 
	 - APISecret – 

	```{r}

envMap.put("CERT", new EnvPropertiesImpl( "CERT", "https://cert.api.firstdata.com/gateway/v1/payments", "---------", "----------", "-----------"));

	``` 
 
gatewayMerchantId and the APIGEE credentials will be provided by the Integration Team.

### Credit Card for Testing

Note that even for testing purpose; the credit card information used in the app must be attached to an active account. 
The standard test cards will not be validated by Google and will fail in processing.

### Execute Authorize and Purchase Request

Fiserv Header Authorization Parameter

The Authorization parameter, required as part of the Header for a Fiserv API transaction, is created as follows:

Construct the data param by appending the following parameters in the order shown:

apikey – the developer’s API key
nonce – A secure random number
timestamp – Epoch timestamp in milliseconds
token – the Merchant Token 
payload – The actual body content passed as the POST request 

### Google Pay APK Installation to Device

	 - Once the downloaded code for the sample app is built successfully in Android Studio, build the APK and install it on your device.
	 - Once the APK is installed, select the Open option to access the application. The screenshots below show the sample application installed on the test device (nonPROD environment), and the response from a payment processed in the First Data nonPROD environment/Google test environment.

Note that the Payment Details page cannot be captured for security reasons.

"https://github.com/Fiserv/ipg-na/blob/637f64ada1a6a751e50b0891403103faff69db79/assets/images/GooglePay1.jpg?raw=true"

Sample Google Pay Request:


```{r}  

{
  "requestType": "WalletSaleTransaction",
  "walletPaymentMethod": {
    "walletType": "EncryptedGooglePayWalletPaymentMethod",
    "encryptedGooglePay": {
      "data": {
        "encryptedMessage": "8nxjB9mr2tWZeDRQRcGN91UUnb7AioGp3oRo8kmQ6lyvJZiqD7PJlbRCYElNqUmr6Z8zK7b2gO9MKOjpnTCqH0qAe2vuIlwNXB60M2Lh7Qfl3bVgWzwF/FfFcenVW381hoItYi8AjWnWoydz1XMTEv2qhqUG03mEnRXdMyDyk6KKZXoW8Qc0p1F1thbxxu8weU8CZbZsWGGTjB42cilIqLVbribcOAG8Oas1AcgefFsu2hwp4gdSuOg7wmeSV7XKsGQzzVy85qtjuqET2XYzJE3K/Wh9QKkhu5P9Ms5s1+Smr2IjRyidqQa88SxQplrVoo9+PvT0bxFcMspBmO3pLkuaZSUBy++dL2fefcxNJvGCFfFhdxW9DojuuQxgpeu7RAQUsGLyFmr/4ZfBxt882xTmpX9MRx5CAudl9qUgBfKdwWwMX35qSbDTm1ju5XXzNh94VebjD3bB9Zj8qgbmUOr/+6OQLhoFJyBCXgx3EEH8hBwNVFrss/SLwQvFhZh62eO6lOtnmbOtP1yTDDVqGDBfai5SwAmM+KTcc9SGv/xDC+cWe8ck+aCBkG4HoRPapUVMZ3JIgV7yzTsVLJE\\u003d",
        "ephemeralPublicKey": "BGH3fRFdoAobYrAlxnZOCYzkH84Cna92IZxtgsU36CMDaqSaDYb9/LsY8qw+vMtlBnwsUg/YVMOeeKp+qDkOWb4\\u003d",
        "tag": "nvmOUNpnOTZULLhMxT/hWCHzH/4f7gGpfvQgwl3p8ng\\u003d"
      },
      "signature": "MEUCIFWTRWUZAOM5nfJC79FtJm56olnbwG4H5uWWxAUWAquiAiEA24j/BcOroeISsdJzYsyoVi8wzu4tnmKw+jdsGfuvPko=",
      "version": "ECv1"
    }
  },
  "transactionAmount": {
    "total": "1200",
    "currency": "USD"
  }
}
```    
	 
 
Sample Google Pay Response:


```{r}  

{
    "clientRequestId": "741666",
    "apiTraceId": "rrt-01b12ed35a0f32f98-c-ea-12855-958124-1",
    "ipgTransactionId": "84290618651",
    "orderId": "R-3f8d4c21-66c9-47d4-bb59-c7f167ace094",
    "transactionType": "SALE",
    "transactionOrigin": "ECOM",
    "paymentMethodDetails": {
        "paymentCard": {
            "expiryDate": {
                "month": "**",
                "year": "****"
            },
            "bin": "******",
            "last4": "****",
            "brand": "AMEX"
        },
        "paymentMethodType": "PAYMENT_CARD"
    },
    "country": "USA",
    "terminalId": "1588390",
    "transactionTime": 1579707422,
    "approvedAmount": {
        "total": 12.00,
        "currency": "USD",
        "components": {
            "subtotal": 12.00
        }
    },
    "transactionStatus": "APPROVED",
    "schemeTransactionId": "010022066071191",
    "processor": {
        "referenceNumber": "84290618651 ",
        "authorizationCode": "OK4090",
        "responseCode": "00",
        "network": "AMEX",
        "associationResponseCode": "000",
        "responseMessage": "APPROVAL",
        "avsResponse": {
            "streetMatch": "Y",
            "postalCodeMatch": "Y"
        }
    },
    "additionalDetails": {
        "walletProvider": "GOOGLE_PAY"
    }
}
``` 
    
	    



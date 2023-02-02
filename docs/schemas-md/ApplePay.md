# Apple Pay

Apple Pay enables secure, simple checkouts in your app or on your website.

User Action: the buyer taps the Apple Pay button in the app or on the website, selects the payment card and uses the Touch-ID to complete the transaction.

 - The Merchant App communicates with the merchant server and creates a transaction ID
 - The Merchant App obtains the encrypted transaction payload (The tokenized card data "DPAN", Cryptogram, and  	transaction details) from Apple's Pass Kit Framework
 - The Merchant App sends the encrypted transaction payload to processor API using the Apple Pay SDK
 - Processor API decrypts the encrypted transaction payload and processes the transaction
 - Processor API responds back to the Merchant App (through the SDK) with either an approval or decline

To get more information on participating banks and countries for Apple Pay, [AuthOptimization](https://support.apple.com/en-us/HT204916)|.

## Apple Pay Integration

## Merchant Boarding

Please reach out to your local Integration Support team for getting your account enabled.

## CSR Generation

Our Integration team will generate the CSR and share it with you along with the Merchant Identifier.

## Generate Payment Processing Certificate from Apple Portal

Steps to create a Payment processing certificate in the Apple portal:

 - Login to apple 'Account' in developer.apple.com
 - In-order to generate certificate you must have a paid apple developer account or an organization account. New users must follow the prompts to set up a developer account.
 - Select Certificates, Identifiers and Profile :  
 
   [Certificates, Identifiers and Profile](assets/images/ApplePay1.jpg)  
   
 - Select Identifier's and in the dropdown in the upper-right corner select merchant id
 - Enter a unique merchant id, and upload a valid CSR in .pem format.
 - Once successfully uploaded, apple provides the payment processing certificate and the merchant id will come up in the certificate section.
 - Download payment processing certificate and install in your computer by double clicking it.
 - The certificate should show up in the 'Key chain access' of your Macbook.

## Upload and register the apple development certificate for your machine

 - Request a new certificate from your keychain access.  
 
   ![Certificate From Your Keychain Access](assets/images/ApplePay2.jpg)  
   
 - Follow the prompt and request the certificate to be saved on file.
 - In the 'Certificate' section in the apple portal, click on the '+' and follow the prompt to request apple developer certificate for 'IOS' development.
 - Upload the requested certificate
 - Download and install the apple pay developer certificate.
 - Your machine is now setup for programming IOS app using Xcode.

## Set-up Provision Profile for the application

 - In the 'Certificate, Identifier and Profile' section in the apple portal navigate to profile.
 - Click the '+' sign to create a new profile.
 - Choose, 'IOS' development and follow the prompts
 - In the capabilities select 'Apple Pay' and 'In-App Purchases'
 - You can also register the test devices here using, uuid. (Xcode also does this when the app is built on the phone)
 - Download the provision profile on to your mac.

## Set-up Project in Xcode

 - Select new xcode project with a single view or import an existing project.
 - Register the app using the app-id in the apple portal under Identifier->appId
 - Go to Xcode->Preferences,->accounts and install the downloaded provision profile, your profile is now linked to your Xcode.
 - Click on your project, go to Signing & Capabilities select 'Automatically manage signing'.
'+ capabilities' add apple pay.
 - Under 'Apple Pay' click '+' and add the merchant id's registered in the portal, which in turn will be added to the entitlements file. 

Now the Xcode is set-up for coding.

In the SDK enter the URL, api key and api secret and build the app:  

   ![Enter URL,API Key and Secret](assets/images/ApplePay3.jpg)
   	  
 - Merchant id: Enter any valid merchant id registered in the apple portal. This gives the capability for a single user to use multiple merchant id's
 - Amount: Enter the amount of the transaction
 - Transaction type: Select PreAuth or Sale.
 - Apple Pay Button: Click this to produce payment sheet and fingerprint authentication for the transaction.
 - Once the user authenticates the transaction the apple returns the payment token, using which the SDK generates the following payload:

 

## Sample Apple Pay Request

Endpoint: https://cert.api.firstdata.com/gateway/v2/payments

```{r}

{

   "walletPaymentMethod":{
      "walletType":"EncryptedApplePayWalletPaymentMethod",
      "encryptedApplePay":{
      "data":"hbreWcQg980mUoUCfuCoripnHO210lvtizOFLV6PTw1DjooSwik778bH/qgK2pKelDTiiC8eXeiSwSIfrTPp6tq9x8Xo2H0KYAHCjLaJtoDdnjXm8QtC3m8MlcKAyYKp4hOW6tcPmy5rKVCKr1RFCDwjWd9zfVmp/au8hzZQtTYvnlje9t36xNy057eKmA1Bl1r9MFPxicTudVesSYMoAPS4IS+IlYiZzCPHzSLYLvFNiLFzP77qq7B6HSZ3dAZm244v8ep9EQdZVb1xzYdr6U+F5n1W+prS/fnL4+PVdiJK1Gn2qhiveyQX1XopLEQSbMDaW0wYhfDP9XM/+EDMLaXIKRiCtFry9nkbQZDjr2ti91KOAvzQf7XFbV+O8i60BSlI4/QRmLdKHmk/m0rDgQAoYLgUZ5xjKzXpJR9iW6RWuNYyaf9XdD8s2eB9aBQ=",

         "header":{
            "applicationDataHash":"94ee059335e587e501cc4bf90613e0814f00a7b08bc7c648fd865a2af6a22cc2",
           "ephemeralPublicKey":"MFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAEvR+anQg6pElOsCnC3HIeNoEs2XMHQwxuy9plV1MfRRtIiHnQ6MyOS+1FQ7WZR2bVAnHFhPFaM9RYe7/bynvVvg==",
            "publicKeyHash":"KRsyW0NauLpN8OwKr+yeu4jl6APbgW05/TYo5eGW0bQ=",
            "transactionId":"31323334353637"
         },
        "signature":"MIAGCSqGSIb3DQEHAqCAMIACAQExDzANBglghkgBZQMEAgEFADCABgkqhkiG9w0BBwEAAKCAMIIB0zCCAXkCAQEwCQYHKoZIzj0EATB2MQswCQYDVQQGEwJVUzELMAkGA1UECAwCTkoxFDASBgNVBAcMC0plcnNleSBDaXR5MRMwEQYDVQQKDApGaXJzdCBEYXRhMRIwEAYDVQQLDAlGaXJzdCBBUEkxGzAZBgNVBAMMEmQxZHZ0bDEwMDAuMWRjLmNvbTAeFw0xNTA3MjMxNjQxMDNaFw0xOTA3MjIxNjQxMDNaMHYxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJOSjEUMBIGA1UEBwwLSmVyc2V5IENpdHkxEzARBgNVBAoMCkZpcnN0IERhdGExEjAQBgNVBAsMCUZpcnN0IEFQSTEbMBkGA1UEAwwSZDFkdnRsMTAwMC4xZGMuY29tMFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAErnHhPM18HFbOomJMUiLiPL7nrJuWvfPy0Gg3xsX3m8q0oWhTs1QcQDTT+TR3yh4sDRPqXnsTUwcvbrCOzdUEeTAJBgcqhkjOPQQBA0kAMEYCIQDrC1z2JTx1jZPvllpnkxPEzBGk9BhTCkEB58j/Cv+sXQIhAKGongoz++3tJroo1GxnwvzK/Qmc4P1K2lHoh9biZeNhAAAxggFSMIIBTgIBATB7MHYxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJOSjEUMBIGA1UEBwwLSmVyc2V5IENpdHkxEzARBgNVBAoMCkZpcnN0IERhdGExEjAQBgNVBAsMCUZpcnN0IEFQSTEbMBkGA1UEAwwSZDFkdnRsMTAwMC4xZGMuY29tAgEBMA0GCWCGSAFlAwQCAQUAoGkwGAYJKoZIhvcNAQkDMQsGCSqGSIb3DQEHATAcBgkqhkiG9w0BCQUxDxcNMTkwNjA3MTg0MTIxWjAvBgkqhkiG9w0BCQQxIgQg0PLaZU4YWZqtP9t/ygv9XIS/5ngU6FlGjpvyK6VFXVMwCgYIKoZIzj0EAwIERjBEAiBTNmQEPyc3aMm4Mwa0riD3dNdSc9aAhslj65Us8b3aKwIgNSc/y+CWpsr8qDln0fZK6ZD/LWPMxofQedlPy7Q6gY8AAAAAAAA=",
         "version":"EC_v1",
         "applicationData":"VEVTVA==",
         "merchantId":"merchant.com.fapi.tcoe.applepay"
      }
   },
   "transactionAmount":{
      "total":"12.99",
      "currency":"USD"
   }
}
```  

## Sample Apple Pay Response

```{r}

{
    "clientRequestId": "741666",
    "apiTraceId": "rrt-01b12ed35a0f32f98-c-ea-12855-958124-1",
    "ipgTransactionId": "84290618651",
    "orderId": "R-3f8d4c21-66c9-47d4-bb59-c7f167ace094",
    "transactionType": "SALE",
    "transactionOrigin": "ECOM",
    "paymentMethodDetails": {
        "expiryDate": {
            "month": "**",
            "year": "****"
        },
        "bin": "******",
        "last4": "****",
        "brand": "AMEX"
    },
    "paymentMethodType": "PAYMENT_CARD",
    "country": "USA",
    "terminalId": "1588390",
    "transactionTime": 1579707422,
    "approvedAmount": {
        "total": 12.00,
        "currency": "USD",
        "components": {
            "subtotal": 12.00
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
            "walletProvider": "APPLE_PAY"
        }
    }
}
``` 

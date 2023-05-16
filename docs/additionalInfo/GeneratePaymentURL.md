
# Generate a Payment URL

The Payment URL functionality allows you to provide a link (URL) to your customers e.g. in an email invoice, WhatsApp message, SMS, QR code, etc. which then takes the customer to a webpage, hosted by Fiserv, where they can securely make the payment with their preferred payment method, whenever convenient for them.

This solution is especially useful in scenarios where goods get paid after delivery, where no goods get shipped at all (e.g. final payment for trips that have been booked months ago) or for the payment of monthly bills.

You can also implement this functionality for unsuccessful purchases where the original payment transaction has been declined so that you can proactively give your customers a second chance to make their purchase.

The Payment URL solution offers you the following:

- The capability to generate a link (a payment URL) for a specific amount through an Application Programming Interface (API) call or manually through a Virtual Terminal on the web.
- A hosted payment page where your customer can select the preferred payment method (based on the payment methods that are activated for your account/store) and make the payment.
- A hosted result page that tells your customer if the payment was successful or not, including a 'Retry' button that allows a customer to choose a different payment method in case the transaction was not successful.

As a default, the Payment Links stay valid for 182 days.

> [Payment URL Customer Experience](?path=docs/additionalInfo/PaymentUrlCustomerExperience.md)

Generate a Payment URL via an API call

If you have IT systems where you want to automate the creation of the Payment Link, Fiserv provides an API that allows you to send transaction type, amount and currency as well as the language that shall be used on the hosted payment page that will be shown to the customer after accessing the link.

|  | |
|----|----|
|POST /payment-url|Use /payment-url to generate a URL that you can send to a customer, which they can then use to pay you.|
|  | |

---------------------------
	     	
### REST API Request Example

```{r}
 
{
  "transactionAmount": {
    "total": "42.42",
    "currency": "USD"
  },
  "transactionType": "SALE",
  "transactionNotificationURL": "https://showmethepaymentresult.com",
  "expiration": "4102358400",
  "authenticateTransaction": true,
  "dynamicMerchantName": "MyWebsite",
  "invoiceNumber": "96126098",
}
 
``` 

The response contains the (paymentUrl) that you can send to your customer:

### REST API Response Example

```{r}

{
  "clientRequestId": "30dd879c-ee2f-11db-8314-0800200c9a66",
  "apiTraceId": "rrt-0bd552c12342d3448-b-ea-1142-12938318-7",
  "requestStatus": "SUCCESS",
  "orderId": "9723846",
  "paymentUrl": "https://hyperlink-to-payment.com",
  "transactionId": "2381723322"
}

```
------------------
> [REST API Reference ](?path=docs/schemas-md/PaymentCardPreAuthTransaction.md)


### Generate a Payment URL using the Virtual Terminal

The Virtual Terminal is a solution that you can access with your Internet browser and log in with a Username and password, just like accessing an email web account. It allows you to enter data for payment transactions and run these manually with a real-time response.

After login into the Virtual Terminal, if you have the Payment URL functionality enabled for your store, you will find an option to select Generate Payment URL under the Order Information section.

If the Generate Payment URL checkbox is selected, the Card section (Credit Card, Direct Debit) and Recurring sections will be hidden. You can then complete the required information for the payment URL and continue the transaction as usual.

The generated link is shown on the 'Transaction Result' page where it can be selected and copied by you in order to be provided to the customer, e.g. in an email invoice you are sending.. The link can also be obtained from the 'Order Details' page at a later point, when needed.

![](/api/hosted-image/IPGNA/assets/images/generatePaymentUrl_1.jpg)

  																   Option to generate a Payment URL

The generated URL will be shown on the Transaction Result page where it can be selected (copied) to provide it to the customer. The URL can also be copied from the Order Details page at a later point.


![](/api/hosted-image/IPGNA/assets/images/generatePaymentUrl_2.jpg)

                                                                   Option to 'Select' in order to copy the link'  

The generated link is shown in real-time reports accessible in the Virtual Terminal with an approval code '?:Payment URL created'.

![](/api/hosted-image/IPGNA/assets/images/generatePaymentUrl_3.jpg)

                                                                   Order Details overview

Once your consumer has accessed the URL link and made the payment, you will see the result of this payment transaction in the reports and the total amount will be updated with the payment made.

![](/api/hosted-image/IPGNA/assets/images/generatePaymentUrl_4.jpg)

                                                   Option to review the status of a payment on 'Order Details' page

API users also have the ability to delete a Payment URL to cancel the validity.  If a deletion has been performed and a consumer selects the URL thereafter they will be presented with display information advising the URL is no longer valid.  You will be able to see the deleted status in the Order Details as below:

![](/api/hosted-image/IPGNA/assets/images/generatePaymentUrl_5.jpg)


* If you are a MCC6012 Merchant you can still utilize this functionality, the additional entries required for MCC6012 will need to be completed at the time of generating the URL and saved to be added to the transaction should the consumer opt to pay with Visa or MasterCard.
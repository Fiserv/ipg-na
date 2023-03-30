

# Recurring Payments

Recurring payments can either be triggered by your system everytime a payment is due or you can make use of our scheduler that allows you to define the frequency and period (e.g. every three days, every second week, every month, once a year, etc.).

## Triggering Recurring Payments

When triggering Recurring Payments through our API, you need to indicate if the transaction you are sending is the first in series or a subsequent transaction.

> [How to process recurring payments with stored credentials](?path=docs/additionalInfo/RecurringPaymentswithStoredCredentials.md)

> [How to process recurring payments with SOAP API](?path=docs/additionalInfo/ProcessRecurringPaymentWithSOAPAPI.md)

## Using the Scheduler

Recurring Payments that shall be periodically triggered by our Gateway can be installed via three different options:

### Option 1:
### Schedule recurring payments using our API

The action RecurringPayment allows you to install, modify or cancel periodic payments in a way that
subsequent transactions will automatically be triggered by the gateway.

For every recurring transaction, the gateway can send a server-to-server transaction notification to a
defined Notification URL. Please contact your local support team to get your URL registered for these
notifications.

### Option 2:

Make payments recurring that get initiated through your website
To use this feature, the following additional parameters will have to be submitted in the transaction request:

| *Field Name* | *Possible Values*|*Description*|
|----|----|----|
|recurringInstallmentCount|Number between 1 and 999|Number of installments to be made including the initial transaction submitted|
|recurringInstallmentPeriod|day<br/>week<br/>month<br/>year|The periodicity of the recurring payment|
|recurringInstallmentFrequency|Number between 1 and 99|The time period between installments|

Note that the start date of the recurring payments will be the current date and will be automatically calculated by the system.

### Option 3:

Make payments recurring that you enter via the Virtual Terminal
The Recurring Payments section in the Virtual Terminal allows you to make a credit card (Sale) transaction recurring.

 1. To make a transaction recurring, select the Yes checkbox next to Make recurring?
 
 2. Next enter how often you wish to charge the customer. In the Bill the customer fields, enter a number from 1 to 999 with no decimal point and select day, week, month, or year in the dropdown box. For example, if you wish to charge the customer once a year, enter the number 1 and select year in the dropdown box. To charge the customer twice a year (once every 6 months), you would enter the number 6 and select month in the dropdown box.
 
 3. Select the month / day / year to start charging the customer in the Start on dropdown boxes.
 
 4. Enter the number of times to charge the customer in the End After textbox.


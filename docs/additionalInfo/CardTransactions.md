
# Enter payment data for card transactions

The *Payment Details* section shows fields required for a Sale, Authorise Only, Forced Ticket or Account authorization transaction.

A graphic for each card type that has been setup for your store is shown.

![](/api/hosted-image/IPGNA/assets/images/cardTransactions.jpg)


                                              Virtual Terminal: Card data input fields 

To enter card information, follow the steps below:

 

### *Step 1: Select the Card Type (optional)*

First, select the card type from the Select card type dropdown box or click on one of the brand logos.

 

### *Step 2: Select the Transaction Origin*

Select the transaction origin from the Transaction Origin dropdown box.

- Select Retail (face to face) if the customer and the card are in your presence.
- Select Electronic Commerce (internet) if the order came to you over the Internet or
  via e-mail.
- Select Mail Order* if you received the order through the mail
- Select Telephone Order if you received the order over the phone.
 

*Transaction Origin* is always a required field therefore you must make a selection.

*To comply with scheme requirements, when Mail Order is selected the Card Security Code field will become inactive and there will be no option to enter one.

 
### *Step 3: Select the Transaction Type*

Once you've selected the transaction origin, select the appropriate transaction type for your card transaction in the Transaction Type dropdown box.

- Select Sale to charge the customer's card immediately (upon batch settlement)
- Authorise Only to reserve funds on the customer's card, but not complete the transaction yet
- Forced Ticket to complete a voice authorisation transaction.
- Account authorization to only validate a card (Visa or MasterCard) with a zero value amount
 

If you need to do any other type of transaction, you'll need to visit another page. To complete an Authorise Only transaction, go to the Completion page. To do a Return, go to the Return or the Credits page.

 

Transaction Type is always a required field, but if you do not make a selection, it defaults to Sale.

 

### *Step 4: Enter the Card Number or Swipe the Card*

Enter the card number in the Card Number field. You may include spaces or dashes if you wish.

 

If the card is present and you have the appropriate reader (configured correctly), place your cursor in the Card Number field, and then swipe the card through the reader. The Card Number field should be automatically filled in for you. If it is, there is no need to enter any other data.

All other required fields (except Transaction origin and Transaction type) become optional because the entire customer's data is passed to us from this one entry.

If something should go wrong and this field does not fill in when you swipe the card, check your reader to make sure it's configured correctly. If the reader is configured correctly and you are still unable to swipe the card, the card may be unreadable. Go to the previous field (Are you swiping the card?), uncheck the Yes checkbox, and enter the card data manually.

Note: If your store has been activated for GlobalChoice™ please click here for further information.

 

### *Step 5: Enter the Expiry Date*

Select the card's Expiry Date from the dropdown boxes. Select the month first, then the year that the card expires.

 

### *Step 6: Enter the Card Security Code*

The Card Security Code is a 3 or 4-digit number usually found on the back of the customer’s credit card, on the same line as the customer’s signature, following the last four digits of the credit card number. There are many different names for this code: Visa calls this code CVV2, MasterCard calls it CVC2, American Express 4DBC.

 

### *Step 7: Enter the Reference Number (required only for Forced Ticket transactions)*

If you are performing a Forced Ticket transaction, enter the reference number associated with this transaction (typically given to you over the phone with the authorisation) in the Reference Number box. The Reference Number field will not appear unless you have chosen Forced Ticket as the transaction type.

 

### *Step 8: Enter the Number of Instalments (optional, if merchant is configured for instalments)*

If your store has been enabled for instalments, you can enter the number of instalments to complete the payment. You must include a numeric field.

 

### *Step 9: Continue to the Customer Contact Information section*

Click on Customer Contact Information to expand the text, and then enter the appropriate fields. The Customer ID is a unique identification number you can choose for the customer.

 

> Return to [Performing a Virtual Terminal Transaction](?path=docs/additionalInfo/VirtualTerminal.md)

> Move on to [Complete the Transaction](?path=docs/additionalInfo/CompleteTheTransaction.md)

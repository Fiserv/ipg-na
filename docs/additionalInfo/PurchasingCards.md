
# Purchasing Cards

Purchasing Cards offer businesses the ability to allow their employees to purchase items with a credit card while providing additional information on sales tax, customer code etc. Providing specific details on the payment being made with a Purchasing card can enable qualification of favourable addendum interchange rates.

There are three levels of details required:

- Level I - The first level is the standard transaction data; no enhanced data is required at this level.
- Level II - The second level requires that data such as tax amount and customer code be supplied in addition to the standard transaction date.  (Visa only have a level II option)
- Level III - The third level allows a merchant to pass a detailed accounting of goods and services purchased to the buyer. All the data for Level I and Level II must also be passed to participate in Level III. (Visa and Mastercard).

Purchasing Cards Level 2 and Level 3 fields are available for transactions processed using the Virtual Terminal. When completing the transaction information.  

![](/api/hosted-image/IPGNA/assets/images/purchasingCards.jpg)

Level 2 can be completed alone for Visa transactions. 

### Level 2 Details

The information for the whole transaction is required

- Customer Reference ID
- Supplier Invoice Number 
- Supplier VAT Registration Number
- Total Discount Amount
- Total Discount Rate
- VAT Shipping Amount
- VAT Shipping Rate
- Complete the fields in the table also, per item purchased, to achieve Level 3.  This is valid for both Visa and MasterCard.

When performing a transation, under the ‘Card’ heading there is a tick box entitled Purchase Cards. Select this box to show the fields for Level 2, and a table for Level 3.  

If you have this option enabled you can decide whether to not complete any specific Purchasing Card detail fields, complete only Level 2 detail or continue on to complete all to achieve Level 3

### Level 3 Details

The information per Item is required

- Product Code - product code of the item purchased
- Description - Text description of the item purchased
- Quantity - Number of units of the item purchased
- Unit - Unit of measure code
- Unit Price - Unit price of the item purchased
- Commodity Code - The commodity code used to classify the item purchased
- VAT Amount - VAT amount for the item purchased
- Rate (%) - VAT % rate
- Discount Amount - Amount of the discount applied to the line item
- Rate (%) - Discount % rate
- Total - Total for the item
 
The button Add Item(s) allows to add lines to the table where information can be provided for further purchased items. 

Complete the remainder of the transaction as usual.

> Return to [Performing a Virtual Terminal Transaction](?path=docs/additionalInfo/VirtualTerminal.md)		
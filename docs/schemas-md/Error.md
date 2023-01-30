
# Error

| *description*:   | *Error information.*|
|----|----|
| code |    ``` string ```  *example: 2303*. Uniquely identifies an error condition. Client applications need to read and handle errors based on this.|
| message |     ``` string ```  *example: Invalid credit card number*. A generic description of the error condition.|
| details | Detailed information about message format errors.|
|         | **field** :  ``` string ```  *example: PaymentCard.number*. The property or attribute associated with the error.|
|         | **message** :  ``` string ```  *example: may not be null*. Information specific to a property or attribute.|
| declineReasonCode |     ``` string ```  *example: Do not try again*.Information about the decline reason.|   




  


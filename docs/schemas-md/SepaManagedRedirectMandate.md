
# SepaManagedRedirectMandate

| *description*:   | *Model for the SEPA Mandate information.*|
|----|----|
| reference |    ``` string ``` <br/> maxLength: 35 <br/> pattern: [A-Za-z0-9:?/+(),. -]{1,35} <br/> *example: 3RBQVEE* <br/> Existing mandate reference, managed by merchant. Must match [A-Za-z0-9:?/+(),. -]{1,35} and not start with two slashes ("//"). Also known as the mandate ID.|
| url |  ``` string ``` <br/> maxLength: 100 <br/> pattern: ^[^\s](?!\s*$).+[^\s]$ <br/> *example: https://www.firstdata.com* <br/> Valid URL pointing to the SEPA mandate (PDF / HTML format recommended). When your store is enabled for SEPA Direct Debit as part of the Local Payments offering, this field allows you to transmit a valid URL of SEPA Direct Debit mandate to enable the Risk and Compliance department to access the details. Please note that it is mandatory to submit a mandateReference and a mandateDate together with a mandateUrl in case you manage SEPA Direct Debit mandates on your side in the combination with the Local Payments offering.  
| signatureDate |  ``` string ``` <br/> *example: 2017-07-15* <br/> Date of mandate signature.|
| type* |  ``` string ``` <br/> default: SINGLE <br/> *example: FINAL_COLLECTION* <br/> Sequence type of the direct debit. This defaults to 'SINGLE' if not provided.|  



     




# SepaManagedRedirectSale

| *description*:   | *The payment object for SEPA Local Payment.*|
|----|----|
| iban* |    ``` string ``` <br/> maxLength: 34 <br/> pattern: ^(?!\s*$).+ <br/> *example: DE34500100600032121604* <br/> Bank account in IBAN format.|
| name* |  ``` string ``` <br/> maxLength: 96 <br/> pattern: ^[^\s](?!\s*$).+[^\s]$ <br/> *example: John Doe* <br/> The name of the payer.|  
| email |  ``` string ``` <br/> maxLength: 254 <br/> *example: john.doe@test.com* <br/> The email address of the payer.|
| mandate* |  [SepaManagedRedirectMandate](?path=docs/schemas-md/SepaManagedRedirectMandate.md)|  



     



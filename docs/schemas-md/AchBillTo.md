
# achBillTo

| *description*: | *Consumer billing address details.For Telecheck Verification service: *Required for U.S Addresses.<br/> For Telecheck Warrant service: *Required. <br/> For help with Telecheck Services, please contact your Fiserv Telecheck Sales Representative.*|
|----|----|
| firstName |    ``` string ```  <br/>  maxLength: 30  <br/>  pattern: (?=.*[^\s])^[^|]+$  <br/> *example: R2-D2*  <br/> Customer billing first name.|
| lastName* |    ``` string ```    <br/> maxLength: 30  <br/> pattern: (?=.*[^\s])^[^|]+$  <br/> *example: O'Calloway*  <br/> Customer billing last name.|
| addressOne* |    ``` string ```    <br/> maxLength: 50  <br/> pattern: (?=.*[^\s])^[^|]+$  <br/> *example: 1234 Line Ave S.*  <br/> Customer billing address, first line.|
| addressTwo |    ``` string ```    <br/> cmaxLength: 30  <br/> pattern: (?=.*[^\s])^[^|]+$  <br/> *example: Ste 602*  <br/> Customer billing address, second line.|
| city* |    ``` string ```    <br/> maxLength: 30  <br/> pattern: (?=.*[^\s])^[^|]+$ <br/>  *example: Atlanta*  <br/> Customer billing city.|
| state* |    ``` string ```   <br/> maxLength: 2  <br/> pattern: ^[A-Z]{2}$  <br/> *example: GA*  <br/> Customer billing state.|
| zip* |    ``` string ```   <br/> maxLength: 11  <br/> pattern: (?=.*[^\s])^[^|]+$  <br/> *example: 30040-1309*  <br/> Customer billing zip code.|
| phone* |    ``` string ```    <br/> maxLength: 10  <br/> pattern: ^[0-9]+$  <br/> *example: 9973322990*  <br/> Customer billing phone number.|
| email |    ``` string ```    <br/> maxLength: 100  <br/> pattern: (?=.*[^\s])^[^|]+$  <br/> *example: abcd.1234@fiserv.com*  <br/> Customer billing email. Required if performing an ICA transaction.|
| countryCode |    ``` string ```    <br/> maxLength: 2  <br/> pattern: ^[A-Z]{2}$  <br/> *example: US*  <br/> ISO country code. Required if performing an ICA transaction.| 








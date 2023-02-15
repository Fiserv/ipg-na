
# achBillTo

| *description*: | *Consumer billing address details.|+For Telecheck Verification service: *Required for U.S Addresses.|+For Telecheck Warrant service: *Required.|+For help with Telecheck Services, please contact your Fiserv Telecheck Sales Representative.*|
|----|----|
| firstName |    ``` string ```   *maxLength: 30 pattern: (?=.*[^\s])^[^|]+$ example: R2-D2* Customer billing first name.|
| lastName* |    ``` string ```   *maxLength: 30 pattern: (?=.*[^\s])^[^|]+$ example: O'Calloway* Customer billing last name.|
| addressOne* |    ``` string ```   *maxLength: 50 pattern: (?=.*[^\s])^[^|]+$ example: 1234 Line Ave S.* Customer billing address, first line.|
| addressTwo |    ``` string ```   *maxLength: 30 pattern: (?=.*[^\s])^[^|]+$ example: Ste 602* Customer billing address, second line.|
| city* |    ``` string ```   *maxLength: 30 pattern: (?=.*[^\s])^[^|]+$ example: Atlanta* Customer billing city.|
| state* |    ``` string ```   *maxLength: 2 pattern: ^[A-Z]{2}$ example: GA* Customer billing state.|
| zip* |    ``` string ```   *maxLength: 11 pattern: (?=.*[^\s])^[^|]+$ example: 30040-1309* Customer billing zip code.|
| phone* |    ``` string ```   *maxLength: 10 pattern: ^[0-9]+$ example: 9973322990* Customer billing phone number.|
| email |    ``` string ```   *maxLength: 100 pattern: (?=.*[^\s])^[^|]+$ example: abcd.1234@fiserv.com* Customer billing email. Required if performing an ICA transaction.|
| countryCode |    ``` string ```   *maxLength: 2 pattern: ^[A-Z]{2}$ example: US* ISO country code. Required if performing an ICA transaction.| 








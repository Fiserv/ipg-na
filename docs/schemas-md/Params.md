
# params

| *description*: | *Additional parameters for authentication redirect.*| 
|----|----|
| payerAuthenticationRequest |  ``` string ```   <br/> *example: c7fb83b8ag...73t4a827t4af8738a* <br/>  Message sent from merchant server to authenticate the cardholder.|
| termURL |  ``` string ```  <br/>   <br/> maxLength: 2048  <br/> *example: https://api.example.com/redirectToAcs*  <br/> Terminal URL for processing request.|
| merchantData |  ``` string ```  <br/>  *example: MD123...sdfk*  <br/> Formatted string encoding transaction time, order ID, and return URL data.|
| acsURL |  ``` string ``` <br/>   *example: "https://3ds-acs.test.modirum.com/mdpayacs/pareq"*  <br/> The URL for the authentication redirect for the merchant.|
| cReq |  ``` string ```  <br/>  *example: ewogICAiYWNzVHJhbnNJRCIgOiAiMDAwMDAwMDAtMDAwNS01YTVhLTgwMDAtMDE2ZmE1NTYzODMyIiwKICAgImNoYWxsZW5nZVdpbmRvd1NpemUiIDogIjAzIiwKICAgIm1lc3NhZ2VUeXBlIiA6ICJDUmVxIiwKICAgIm1lc3NhZ2VWZXJzaW9uIiA6ICIyLjEuMCIsCiAgICJ0aHJlZURTU2VydmVyVHJhbnNJRCIgOiAiZGVmOWZiZDgtZjkzNS01YzcyLTgwMDAtMDAwMDAwMDgyOWVkIgp9*  <br/> The CReq message initiates cardholder interaction in a 3DS 2.x challenge flow and carries authentication data from the cardholder.|
| sessionData |  ``` string ```  *maxLength: 6 pattern: ^([1-9][0-9]{0,5})$ example: 1920* Total width of the cardholder’s screen in pixels.|
| browserTimeZone |  ``` string ``` <br/>   *maxLength: 5 example: -300*  <br/> Browser time zone (zone offset value in minutes).|
| browserUserAgent |  ``` string ```  <br/>  *example: 50F2156E03083CA665BCB4..*  <br/> Customer web browser session data.|


  







# params

| *description*: | *Additional parameters for authentication redirect.*| 
|----|----|
| payerAuthenticationRequest |  ``` string ```  *example: c7fb83b8ag...73t4a827t4af8738a* Message sent from merchant server to authenticate the cardholder.|
| termURL |  ``` string ```  *maxLength: 2048 example: https://api.example.com/redirectToAcs* Terminal URL for processing request.|
| merchantData |  ``` string ```  *example: MD123...sdfk* Formatted string encoding transaction time, order ID, and return URL data.|
| acsURL |  ``` string ```  *example: "https://3ds-acs.test.modirum.com/mdpayacs/pareq"* The URL for the authentication redirect for the merchant.|
| cReq |  ``` string ```  *example: ewogICAiYWNzVHJhbnNJRCIgOiAiMDAwMDAwMDAtMDAwNS01YTVhLTgwMDAtMDE2ZmE1NTYzODMyIiwKICAgImNoYWxsZW5nZVdpbmRvd1NpemUiIDogIjAzIiwKICAgIm1lc3NhZ2VUeXBlIiA6ICJDUmVxIiwKICAgIm1lc3NhZ2VWZXJzaW9uIiA6ICIyLjEuMCIsCiAgICJ0aHJlZURTU2VydmVyVHJhbnNJRCIgOiAiZGVmOWZiZDgtZjkzNS01YzcyLTgwMDAtMDAwMDAwMDgyOWVkIgp9* The CReq message initiates cardholder interaction in a 3DS 2.x challenge flow and carries authentication data from the cardholder.|
| sessionData |  ``` string ```  *maxLength: 6 pattern: ^([1-9][0-9]{0,5})$ example: 1920* Total width of the cardholder’s screen in pixels.|
| browserTimeZone |  ``` string ```  *maxLength: 5 example: -300* Browser time zone (zone offset value in minutes).|
| browserUserAgent |  ``` string ```  *example: 50F2156E03083CA665BCB4..* Customer web browser session data.|


  







# cardHolderBrowserParams

| *description*: | *The browser parameters of the cardholder*| 
|----|----|
| browserAcceptHeaders* |  ``` string ```  <br/> maxLength: 2048  <br/> *example: Accept: text/html, application/xhtml+xml, application/xml;q=0.9, image/webp, */*;q=0.8.*  <br/> Browser accept headers.|
| browserIP |  ``` string ```  <br/> maxLength: 45 <br/> *example: 192.168.2.1* <br/>  Browser IP address (IPv4 or IPv6).|
| browserLanguage |  ``` string ```   <br/> maxLength: 8 <br/> *example: es-419*  <br/> Value representing the browser language as defined in IETF BCP47.|
| browserColorDepth |  ``` string ```   <br/> *example: 24* <br/>  Value representing the bit depth of the colour palette for displaying images, in bits per pixel. <br/>  Enum:Array [ 8 ] - [ 1, 4, 8, 15, 16, 24, 32, 48 ]|
| browserScreenHeight |  ``` string ```   <br/> maxLength: 6 <br/> pattern: ^([1-9][0-9]{0,5})$ <br/> *example: 1080* <br/>  Total height of the Cardholder’s screen in pixels.|
| browserScreenWidth |  ``` string ```   <br/> maxLength: 6 <br/>  pattern: ^([1-9][0-9]{0,5})$ <br/> *example: 1920* <br/>  Total width of the cardholder’s screen in pixels.|
| browserTimeZone |  ``` string ```   <br/> maxLength: 5 <br/> *example: -300*  <br/> Browser time zone (zone offset value in minutes).|
| browserUserAgent |  ``` string ```   <br/> maxLength: 2048 <br/> *example: Lynx/2.8.4rel.1 libwww-FM/2.14 SSL-MM/1.4.1 OpenSSL/0.9.6c*  <br/> The browsers user agent string.|  






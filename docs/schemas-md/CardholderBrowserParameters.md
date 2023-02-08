
# CardholderBrowserParameters

| *description*: | *Contains the cardholders browser parameters*| 
|----|----|
| browserAcceptHeaders |  ``` string ```  *maxLength: 2048 example: Accept: text/html, application/xhtml+xml, application/xml;q=0.9, image/webp, */*;q=0.8* Browser accept headers|
| browserLanguage |  ``` string ```  *maxLength: 8 example: es-419* Value representing the browser language as defined in IETF BCP47|
| browserColorDepth |  ``` string ```  *example: 24* Value representing the bit depth of the colour palette for displaying images, in bits per pixel. Enum:Array [ 8 ] - [ 1, 4, 8, 15, 16, 24, 32, 48 ]|
| browserScreenHeight |  ``` string ```  *maxLength: 6 pattern: ^([1-9][0-9]{0,5})$ example: 1080* Total height of the Cardholder’s screen in pixels|
| browserScreenWidth |  ``` string ```  *maxLength: 6 pattern: ^([1-9][0-9]{0,5})$ example: 1920* Total width of the cardholder’s screen in pixels.|
| browserTimeZone |  ``` string ```  *maxLength: 5 example: -300* Browser time zone (zone offset value in minutes).|
| browserUserAgent |  ``` string ```  *maxLength: 2048 example: Lynx/2.8.4rel.1 libwww-FM/2.14 SSL-MM/1.4.1 OpenSSL/0.9.6c* The browsers user agent string| 

**CardholderBrowserParameters Example:** 

```{r}

{
  "browserAcceptHeaders": "Accept: text/html, application/xhtml+xml, application/xml;q=0.9, image/webp, */*;q=0.8",
  "browserIP": "85.117.56.12",
  "browserLanguage": "es-419",
  "browserColorDepth": "32",
  "browserScreenHeight": "1080",
  "browserScreenWidth": "1920",
  "browserTimeZone": "-300",
  "browserUserAgent": "Lynx/2.8.4rel.1 libwww-FM/2.14 SSL-MM/1.4.1 OpenSSL/0.9.6c"
}
```
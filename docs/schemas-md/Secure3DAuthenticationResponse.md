
# Secure3DAuthenticationResponse

| *description*: | *Encapsulates 3DS authentication details in transaction responses.*| 
|----|----|
| type* |  ``` string ```  <br/> *example: 3D_SECURE*  <br/> The type of authentication. <br/>  Enum:Array [ 1 ] - [ 3D_SECURE ]|
| version |  ``` string ```  <br/>  *example: 2.1*  <br/> The version of 3DS used to authenticate.  <br/> Enum:Array [ 3 ] - [ 1.0, 2.1, 2.2 ]|
| params | {[params](?path=docs/schemas-md/Params.md)}| 
| secure3dMethod | {[secure3dMethod](?path=docs/schemas-md/Secure3dMethod.md)}| 

**Secure3DAuthenticationResponse Example:**

```{r}

{
  "type": "3D_SECURE",
  "version": "2.1",
  "redirectURL": "http://pay.issuer-bank.com/sessionID=123&sharedKey=456",
  "secure3dMethod": {
    "methodForm": "&lt;!DOCTYPE iframe SYSTEM \"about:legacy-compat\"&gt; &lt;iframe id=\"tdsMmethodTgtFrame\" name=\"tdsMmethodTgtFrame\"\n                         style=\"width: 1px; height: 1px; display: none;\" src=\"javascript:false;\" xmlns=\"http://www.w3.org/1999/xhtml\"&gt;\n                &lt;!--.--&gt; &lt;/iframe&gt;&lt;form id=\"tdsMmethodForm\" name=\"tdsMmethodForm\"\n                         action=\"https://localhost.modirum.com:8543/dstests/ACSEmu2\" method=\"post\"\n                         target=\"tdsMmethodTgtFrame\" xmlns=\"http://www.w3.org/1999/xhtml\"&gt; &lt;input type=\"hidden\" name=\"3DSMethodData\"\n                         value=\"eyAidGhyZWVEU1NlcnZlclRyYW5zSUQiIDogIjAwMDAwMDAwLTU2NzYtNTY2My04MDAwLTAwMDAw\n                &amp;#10;MDAwNDFhOSIsICJ0aHJlZURTTWV0aG9kTm90aWZpY2F0aW9uVVJMIiA6ICJodHRwczovL2xvY\n                         2Fs&amp;#10;aG9zdC5tb2RpcnVtLmNvbTo4NTQzL21kcGF5bXBpL01lcmNoYW50U2VydmVyP21uPVkmdHhpZD0x\n                &amp;#10;NjgwOSZkaWdlc3Q9aSUyQnhhUEF5NWFOcVJRbllqNmozbWFDZlFJbTdFdjJYTmkwNn\n                         h6YmZNJTJG&amp;#10;R3MlM0QiIH0\"/&gt; &lt;input type=\"hidden\" name=\"threeDSMethodData\"\n                         value=\"eyAidGhyZWVEU1NlcnZlclRyYW5zSUQiIDogIjAwMDAwMDAwLTU2NzYtNTY2My04MDAwLTAwMDA\n                         w&amp;#10;MDAwNDFhOSIsICJ0aHJlZURTTWV0aG9kTm90aWZpY2F0aW9uVVJMIiA6ICJodHRwczovL2xvY\n                         2Fs&amp;#10;aG9zdC5tb2RpcnVtLmNvbTo4NTQzL21kcGF5bXBpL01lcmNoYW50U2VydmVyP21uPVkmd\n                         HhpZD0x&amp;#10;NjgwOSZkaWdlc3Q9aSUyQnhhUEF5NWFOcVJRbllqNmozbWFDZlFJbTdFdjJYTmkwNn\n                         h6YmZNJTJG&amp;#10;R3MlM0QiIH0\"/&gt;\n                &lt;/form&gt;&lt;script type=\"text/javascript\" xmlns=\"http://www.w3.org/1999/xhtml\"&gt;\n                         document.getElementById(\"tdsMmethodForm\").submit(); &lt;/script&gt;"
  },
  "secure3dTransId": "3ac7caa7-aa42-2663-791b-2ac05a542c4a"
}
```  


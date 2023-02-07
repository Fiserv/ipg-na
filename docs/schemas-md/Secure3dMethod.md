
# secure3dMethod

| *description*: | *Encapsulates the 3DS method form and unique transaction identifier.*| 
|----|----|
| payerAuthenticationRequest |  ``` string ```  *example: &lt;!DOCTYPE iframe SYSTEM "about:legacy-compat"&gt; &lt;iframe id="tdsMmethodTgtFrame" name="tdsMmethodTgtFrame" style="width: 1px; height: 1px; display: none;" src="javascript:false;" xmlns="http://www.w3.org/1999/xhtml"&gt; &lt;!--.--&gt; &lt;/iframe&gt;&lt;form id="tdsMmethodForm" name="tdsMmethodForm" action="https://localhost.modirum.com:8543/dstests/ACSEmu2" method="post" target="tdsMmethodTgtFrame" xmlns="http://www.w3.org/1999/xhtml"&gt; &lt;input type="hidden" name="3DSMethodData" value="eyAidGhyZWVEU1NlcnZlclRyYW5zSUQiIDogIjAwMDAwMDAwLTU2NzYtNTY2My04MDAwLTAwMDAw &amp;#10;MDAwNDFhOSIsICJ0aHJlZURTTWV0aG9kTm90aWZpY2F0aW9uVVJMIiA6ICJodHRwczovL2xvY 2Fs&amp;#10;aG9zdC5tb2RpcnVtLmNvbTo4NTQzL21kcGF5bXBpL01lcmNoYW50U2VydmVyP21uPVkmdHhpZD0x &amp;#10;NjgwOSZkaWdlc3Q9aSUyQnhhUEF5NWFOcVJRbllqNmozbWFDZlFJbTdFdjJYTmkwNn h6YmZNJTJG&amp;#10;R3MlM0QiIH0"/&gt; &lt;input type="hidden" name="threeDSMethodData" value="eyAidGhyZWVEU1NlcnZlclRyYW5zSUQiIDogIjAwMDAwMDAwLTU2NzYtNTY2My04MDAwLTAwMDA w&amp;#10;MDAwNDFhOSIsICJ0aHJlZURTTWV0aG9kTm90aWZpY2F0aW9uVVJMIiA6ICJodHRwczovL2xvY 2Fs&amp;#10;aG9zdC5tb2RpcnVtLmNvbTo4NTQzL21kcGF5bXBpL01lcmNoYW50U2VydmVyP21uPVkmd HhpZD0x&amp;#10;NjgwOSZkaWdlc3Q9aSUyQnhhUEF5NWFOcVJRbllqNmozbWFDZlFJbTdFdjJYTmkwNn h6YmZNJTJG&amp;#10;R3MlM0QiIH0"/&gt; &lt;/form&gt;&lt;script type="text/javascript" xmlns="http://www.w3.org/1999/xhtml"&gt; document.getElementById("tdsMmethodForm").submit(); &lt;/script&gt;  An iframe to be hidden in the browser used to collect browser data for the issuers. This information adds to the overall consumer profile and helps in identifying potentially fraudulent transactions.|
| termURL |  ``` string ```  *example: 3ac7caa7-aa42-2663-791b-2ac05a542c4a* A unique transaction identifier supplied by the ACS.|



  






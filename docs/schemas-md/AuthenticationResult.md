
# AuthenticationResult

| *description*:   | *Submit the result of 3DS authentication managed outside of the gateway. <br/> An AuthenticationResult should not be submitted within the same request as an AuthenticationRequest.  <br/> Abstract class, do not use this class directly, use one of its children.*|
|----|----|
| authenticationType |     ``` string ``` <br/> *example: Secure3DAuthenticationResult*  <br/> Specifies the version of 3DS to be used where authentication was managed outside of the gateway.|

**AuthenticationRequest Example:**

```{r}

{
    "authenticationType": "Secure3DAuthenticationResult" 
}
```

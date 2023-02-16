
# AuthenticationRequest

| *description*:   | *Request authentication of the payment card to verify the cardholder and be eligible for liability shift. <br/> An AuthenticationRequest should not be submitted with in the same request as an AuthenticationResult. Abstract class, do not use this class directly, use one of its children.*|
|----|----|
| authenticationType |     ``` string ``` <br/> *example: UnionPayAuthenticationRequest*  <br/> Indicates what kind of authentication scheme the merchant wants to use on the card.|

**AuthenticationRequest Example:**

```{r}

{
    "authenticationType": "UnionPayAuthenticationRequest"
}
```

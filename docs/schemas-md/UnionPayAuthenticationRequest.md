
# UnionPayAuthenticationRequest

| *description*: | *Request authentication of the payment card using the UnionPay SMS scheme.*| 
|----|----|
| authenticationType* |  ``` string ```  <br/>  *example: UnionPayAuthenticationRequest.* <br/>  Indicates what kind of authentication scheme the merchant wants to use on the card.|
| smsPhoneNumber |  ``` string ```  <br/>  *minLength: 7  <br/> pattern: ^(?!\s*$).+ example: 86-13012345678*  <br/> Mobile number for SMS verification.|

**UnionPayAuthenticationRequest Example:**

```{r}

{
  "authenticationType": "UnionPayAuthenticationRequest",
  "smsPhoneNumber": "86-13012345678"
}
```  


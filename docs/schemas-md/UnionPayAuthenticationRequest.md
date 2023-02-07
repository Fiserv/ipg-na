
# UnionPayAuthenticationRequest

| *description*: | *Request authentication of the payment card using the UnionPay SMS scheme.*| 
|----|----|
| authenticationType* |  ``` string ```  *example: UnionPayAuthenticationRequest.* Indicates what kind of authentication scheme the merchant wants to use on the card.|
| smsPhoneNumber |  ``` string ```  *minLength: 7 pattern: ^(?!\s*$).+ example: 86-13012345678* Mobile number for SMS verification.|

**UnionPayAuthenticationRequest Example:**

```{r}

{
  "authenticationType": "UnionPayAuthenticationRequest",
  "smsPhoneNumber": "86-13012345678"
}
```  


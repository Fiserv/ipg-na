
# IdInfo

| *description*: | *Identification information.*|
|----|----|
| idType |    ``` string ```   <br/>  maxLength: 2  <br/> *example: DL*  <br/> Identification type.|
| idData | ``` string ``` <br/> minLength: 1 <br/>  maxLength: 35  <br/> example: 12345678*  <br/> Identification data. |

**IdInfo Example:**

```{r}

{
  "idType": "DL",
  "idData": "12345678"
}
```  






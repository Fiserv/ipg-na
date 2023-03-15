
# AVSResponse

| *description*: | *The processor address validation response for compliance.*| 
|----|----|
| streetMatch |  ``` string ```  <br/>  *example: Y*  <br/> Response if street matches that on file. <br/> Enum:Array [ 4 ] - [ Y, N, NO_INPUT_DATA, NOT_CHECKED ]|
| postalCodeMatch |  ``` string ```   <br/> *example: N* Response if postal code matches that on file.  <br/> Enum:Array [ 4 ] - [ Y, N, NO_INPUT_DATA, NOT_CHECKED ]|
| associationAvsResponse |  ``` string ```  <br/>  *example: N* <br/>  The raw address verification response code returned by issuer. Please refer to  [Response Codes](?path=docs/additionalInfo/ResponseCodes.md) for more info.|

**AVSResponse Example:**

```{r}

{
  "streetMatch": "Y",
  "postalCodeMatch": "N",
  "associationAvsResponse": "Y"
}
```

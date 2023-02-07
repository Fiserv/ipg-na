
# AVSResponse

| *description*: | *The processor address validation response for compliance.*| 
|----|----|
| streetMatch |  ``` string ```  *example: Y* Response if street matches that on file.Enum:Array [ 4 ] - [ Y, N, NO_INPUT_DATA, NOT_CHECKED ]|
| postalCodeMatch |  ``` string ```  *example: N* Response if postal code matches that on file. Enum:Array [ 4 ] - [ Y, N, NO_INPUT_DATA, NOT_CHECKED ]|
| associationAvsResponse |  ``` string ```  *example: N* The raw address verification response code returned by issuer. Please refer to response codes section in developer portal for more info.|

**AVSResponse Example:**

```{r}

{
  "streetMatch": "Y",
  "postalCodeMatch": "N",
  "associationAvsResponse": "Y"
}
```

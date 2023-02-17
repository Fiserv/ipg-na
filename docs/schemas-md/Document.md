
# Document

| *description*:   | *Document information.*|
|----|----|
| type* |    ``` string ```  <br/>  *example: NATIONAL_IDENTITY*  <br/> Document type.  <br/> Enum:[ NATIONAL_IDENTITY, SINGLE_TAX_IDENTIFICATION, SINGLE_CODE_OF_LABOR_IDENTIFICATION, BOOK_ENLISTMENT, CIVIC_NOTEBOOK, PASSPORT ]|
| number* |    ``` string ```  <br/>  maxLength: 30  <br/> *pattern: ^(?!\s*$).+ example: 12345666544*  <br/> Document number.|

**Document Example:**

```{r}

{
  "type": "NATIONAL_IDENTITY",
  "number": "12345666544"
}
``` 

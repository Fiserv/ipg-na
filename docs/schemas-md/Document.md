
# Document

| *description*:   | *Document information.*|
|----|----|
| type* |    ``` string ```  *example: NATIONAL_IDENTITY* Document type. Enum:[ NATIONAL_IDENTITY, SINGLE_TAX_IDENTIFICATION, SINGLE_CODE_OF_LABOR_IDENTIFICATION, BOOK_ENLISTMENT, CIVIC_NOTEBOOK, PASSPORT ]|
| number* |    ``` string ```  *maxLength: 30 pattern: ^(?!\s*$).+ example: 12345666544* Document number.|

**Document Example:**

```{r}

{
  "type": "NATIONAL_IDENTITY",
  "number": "12345666544"
}
``` 

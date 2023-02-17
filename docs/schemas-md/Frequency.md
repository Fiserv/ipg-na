
# Frequency

| *description*:   | *How often payments are sent.*|
|----|----|
| every |     ``` integer ```  <br/> ($int32)  <br/> minimum: 1  <br/> maximum: 1000   <br/> *example: 10*.  Rate of frequency.|
| unit |    ``` string ```  <br/>  *example: MONTH*. <br/>  Unit which defines the frequency.  <br/> Enum:Array [ 4 ] - [ DAY, WEEK, MONTH, YEAR ]|

**Frequency Example:**

```{r}

{
  "every": 3,
  "unit": "DAY"
}
```


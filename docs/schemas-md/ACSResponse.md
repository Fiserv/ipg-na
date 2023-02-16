
# ACSResponse

| *description*: | *Encapsulates response data from the ACS.*| 
|----|----|
| cRes |  ``` string ```   <br/> *example: ewogICAiYWNzUmVmZXJlbmNlTnVtYmVyIiA6ICJBQ1NFbXUyIiwKICAgImFjc1RyYW5zSUQiIDogIjAwMDAwMDAwLTAwMDUtNWE1YS04MDAwLTAxNmZhNTU2MzgzMiIsCiAgICJtZXNzYWdlVHlwZSIgOiAiQ1JlcyIsCiAgICJtZXNzYWdlVmVyc2lvbiIgOiAiMi4xLjAiLAogICAidGhyZWVEU1NlcnZlclRyYW5zSUQiIDogImRlZjlmYmQ4LWY5MzUtNWM3Mi04MDAwLTAwMDAwMDA4MjllZCIsCiAgICJ0cmFuc1N0YXR1cyIgOiAiWSIKfQ*  <br/> The ACS response to the CReq message. It can indicate the result of cardholder authentication or, in the case of an app-based model, also signal that further cardholder interaction is required to complete the authentication.|


**ACSResponse Example:**

```{r}

{
  "cRes": "ewogICAiYWNzUmVmZXJlbmNlTnVtYmVyIiA6ICJBQ1NFbXUyIiwKICAgImFjc1RyYW5zSUQiIDogIjAwMDAwMDAwLTAwMDUtNWE1YS04MDAwLTAxNmZhNTU2MzgzMiIsCiAgICJtZXNzYWdlVHlwZSIgOiAiQ1JlcyIsCiAgICJtZXNzYWdlVmVyc2lvbiIgOiAiMi4xLjAiLAogICAidGhyZWVEU1NlcnZlclRyYW5zSUQiIDogImRlZjlmYmQ4LWY5MzUtNWM3Mi04MDAwLTAwMDAwMDA4MjllZCIsCiAgICJ0cmFuc1N0YXR1cyIgOiAiWSIKfQ"
}
```  
  


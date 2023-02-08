
# DecoupledAuthenticationParameters

| *description*: | *Contains the decoupled authentication parameters*| 
|----|----|
| decMaxTime* |  ``` integer ```  *($int32) minimum: 1 maximum: 10080 example: 10* Indicates the maximum amount of time that the 3DS Requestor will wait for an ACS to provide the results of a Decoupled Authentication transaction (in minutes).|
| decReqInd* |  ``` string ```  *example: Y* Indicates whether the 3DS Requestor requests the ACS to utilise Decoupled Authentication and agrees to utilise Decoupled Authentication if the ACS confirms its use. 'Y' = Decoupled Authentication is supported and preferred if challenge is necessary. 'N' = Do not use Decoupled Authentication. Enum:Array [ 2 ] - [ Y, N ]|


**DecoupledAuthenticationParameters Example:**

```{r}

{
  "decMaxTime": 10,
  "decReqInd": "Y"
}
```

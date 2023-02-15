
# AvailableIsoCountriesResponse

| *description*: | *Full list of available ISO countries.*|
|----|----|
| clientRequestId |    ``` string ```   *example: 30dd879c-ee2f-11db-8314-0800200c9a66* Echoes back the value in the request header for tracking.|
| apiTraceId |    ``` string ```   *example: rrt-0bd552c12342d3448-b-ea-1142-12938318-7* Request identifier in API, can be used to request logs from the support team.|
| responseType | [ResponseType](?path=docs/schemas-md/ResponseType.md)|  
| defaultCountry | [StoreCountry](?path=docs/schemas-md/StoreCountry.md)|
| countries | [  [StoreCountry](?path=docs/schemas-md/StoreCountry.md)  ]|

**AvailableIsoCountriesResponse Example:**

```{r}

{
    "clientRequestId": "30dd879c-ee2f-11db-8314-0800200c9a66",
    "apiTraceId": "rrt-0bd552c12342d3448-b-ea-1142-12938318-7",
    "defaultStoreCountry": OrderedMap {
        "iso31661Alpha2": "US",
        "iso31661Alpha3": "USA",
        "iso31661Numeric": "840",
        "defaultCountry": true
    },
    "countries": List [ OrderedMap {
            "iso31661Alpha2": "US",
            "iso31661Alpha3": "USA",
            "iso31661Numeric": "840",
            "defaultCountry": true
        }, OrderedMap {
            "iso31661Alpha2": "DM",
            "iso31661Alpha3": "DMA",
            "iso31661Numeric": "212",
            "defaultCountry": false
        }
    ]
}
```







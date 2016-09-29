## Retrieve a list of all gear (hardware or software)

Returns a list of all gear currently available, either hardware or software.

**Note** - these lists will be extremely long. 

### Endpoint

For hardware:  
`/api/v1/hardware`

For software:  
`/api/v1/software`  

### Method and URL

For hardware:  
`GET https://usesthis.com/api/v1/hardware/`

For software:  
`GET https://usesthis.com/api/v1/software/`

### Sample Request

For hardware:  
`curl -X GET  "https://usesthis.com/api/v1/hardware/"`

For software:  
`curl -X GET  "https://usesthis.com/api/v1/software/"`


### Sample Response
(Same response format for either `hardware` or `software`)

```json
{
  "gear": [
    {
      "slug": "01v",
      "name": "01V"
    },
    {
      "slug": "055xprob",
      "name": "055XPROB"
    },
    {
      "slug": "1",
      "name": 1
    },
  ]
}
```


| Element     |   Description   |   Type   |   Notes   |
|-------------|-----------------|----------|-----------|
|  **gear**  |    List of gear        |  JSON array   |  &nbsp;    |
|  gear/**slug**  |    Page ID    |  string   |  Will be in "dashed-word-format" if more than one word   |
|  gear/**name**  |    Gear name        |  string   |  Will be a proper name    |



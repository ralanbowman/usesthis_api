## Retrieve a list of all gear (hardware or software) for a category 

Returns a list of all interviews for a specific piece of hardware or software.

### Endpoint

For hardware:  
`/api/v1/hardware/{slug}`

For software:  
`/api/v1/software/{slug}`  

**Note** - a ***slug*** is a short label for an article that is used as part of a URL, usually derived from the title. See **Retrieve a list of all gear (hardware or software)** to get a full list of available slugs.

### Method and URL

For hardware:  
`GET https://usesthis.com/api/v1/hardware/{slug}`

For software:  
`GET https://usesthis.com/api/v1/software/{slug}`

### Sample Request

For hardware:  
`curl -X GET  "https://usesthis.com/api/v1/hardware/iphone/"`

For software:  
`curl -X GET  "https://usesthis.com/api/v1/software/ios"`


### Sample Response
(Same response format for either `hardware` or `software`)


```json
{
  "gear": {
    "slug": "ios",
    "name": "iOS",
    "description": "A mobile operating system.",
    "url": "http://www.apple.com/ios/",
    "interviews": [
      {
        "slug": "rachel.hyman",
        "name": "Rachel Hyman"
      }
    ]
  }
}
```

| Element     |   Description   |   Type   |   Notes   |
|-------------|-----------------|----------|-----------|
|  **gear**  |    List of gear   |  JSON object   |  &nbsp;    |
|  gear/**slug**  |    Page ID    |  string   |   Will be in "dashed-word-format" if more than one word   |
|  gear/**name**  |    Gear name    |  string   |  Will be a proper name    |
|  gear/**description**  |   Short description     |  string   |  &nbsp;    |
|  gear/**url**  |    Vendor website    |  string   |  &nbsp;    |
|  gear/**interviews**  |    All related interviews  |  JSON array   |  &nbsp;    |
|  gear/interviews/**slug**  |    Page ID   |  string   |  In "first.last" name format    |
|  gear/interviews/**name**  |    Full name        | string   |  First and last name    |





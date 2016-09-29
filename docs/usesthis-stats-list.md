## Retrieve the top 50 hardware or software items listed (can also specify year)

Returns a list of the top 50 hardware or software items listed on the site, with counts for each item. The year can also be specified to show counts for that year. 

### Endpoint

For hardware:  
`/api/v1/stats/hardware`

For software:  
`/api/v1/stats/software`

**To show the year:**

For hardware:  
`/api/v1/stats/hardware/YYYY/`

For software:  
`/api/v1/stats/software/YYYY/`

### Method and URL

For hardware:  
`GET https://usesthis.com/api/v1/stats/hardware`

For software:  
`GET https://usesthis.com/api/v1/stats/software`

### Sample Request

For hardware:  
`curl -X GET https://usesthis.com/api/v1/stats/hardware/`

For software:  
`curl -X GET https://usesthis.com/api/v1/stats/software/`

### Sample Response
(Same response format for either `hardware` or `software`)

```json
{
  "gear": [
    {
      "slug": "photoshop",
      "count": 285
    },
    {
      "slug": "chrome",
      "count": 209
    },
    {
      "slug": "dropbox",
      "count": 195
    }
  ]
}
```


| Element     |   Description   |   Type   |   Notes   |
|-------------|-----------------|----------|-----------|
|  **gear**  |    List of gear    |  JSON array   |  &nbsp;    |
|  gear/**slug**  |    Page ID        |  string   |  Will be in "dashed-word-format" if more than one word    |
|  gear/**count**  |    Number of times gear is mentioned  |  integer   |  &nbsp;    |


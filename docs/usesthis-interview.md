## Retrieve a specific interview, including gear

Return a specific interview for a given *slug*, including gear (hardware and software used).

### Endpoint

`/api/v1/interviews/{slug}`

**Note** - a ***slug*** is a short label for an article that is used as part of a URL, usually derived from the title. See **Retrieve a list of all interviews** to get a full list of available slugs.

### Method and URL

`GET https://usesthis.com/api/v1/interviews/{slug}`


### Sample Request

`curl -X GET "https://usesthis.com/api/v1/interviews/jessamyn.west/"`


### Sample Response

```json
{
    "interview": {
        "slug": "slug.name",
        "name": "Slug Name",
        "url": "http://usesthis.com/interviews/slug.name/",
        "summary": "maker, programmer",
        "date": 1458025200,
        "categories": [
            "maker",
            "programmer",
            "mac",
            "linux",
        ],
        "credits": {
            "name": "Photographer (© 2014)"
        },
        "contents": "#### Who are you, and what do you do?\n\n[I'm](http://example.com/ \"Example's website.\") a maker, and a programmer... (output truncated)",
    "gear":{
      "hardware":[
        {
          "slug":"macbook-air",
          "name":"Macbook Air",
          "description":"A very thin laptop.",
          "url":"http://www.apple.com/macbook-air/"
        },
        {
          "slug":"imac",
          "name":"iMac",
          "description":"An all-in-one computer.",
          "url":"http://www.apple.com/imac/"
        },
      ]
    }
  }
}
```


| Element     |   Description   |   Type   |   Notes   |
|-------------|-----------------|----------|-----------|
|  **interviews**  |  Basic interview information   |   JSON array   |  |
|  interviews/**slug**  |    Page ID    |  string   |  In "first.last" name format    |
|  interviews/**name**  |    Full name  |  string   |  First and last name    |
|  interviews/**url**  |    Link to full interview        |  string   |  |
|  interviews/**summary**  |    Summary of the interview        |  string   |  |
|  interviews/**date**  |    Date interview was posted  |  integer   |  **date** is in UNIX epoch time    |
|  interviews/**categories**  |    List of categories for the interview  |  JSON array   |  |
|  interviews/**credits**  |    Photo credit for interview picture    |  JSON object   |  Credit is only listed when provided by subject    |
|  interviews/credits/**name**  |    Name of photographer        |  string   |  &nbsp;    |
|  interviews/**contents**  |    Interview contents, in Markdown format  |  string   |  &nbsp;    |
|  interviews/**gear**  |    List of hardware and software  |  JSON array   |  &nbsp;  |
|  interviews/gear/**hardware**  |  Hardware used      |  JSON object   |  &nbsp;    |
|  interviews/gear/**software**  |    Software used    |  JSON object   |  &nbsp;    |


---

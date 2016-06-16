## Retrieve a list of all interviews

Returns a basic list of all interviews currently available. 

**Note** - this will return a very long list of items.

### Endpoint

`/v1/interviews`  

### Method and URL

`GET https://usesthis.com/api/v1/interviews`  

### Sample Request

`curl -X GET "https://usesthis.com/api/v1/interviews"`

### Sample Response

```json
{
  "interviews": [
    {
      "slug": "nina.freeman",
      "name": "Nina Freeman",
      "url": "http://usesthis.com/interviews/nina.freeman/",
      "summary": "Level designer (Fullbright), game designer (Cibele)",
      "date": 1458198000,
      "categories": [
        "developer",
        "designer",
        "game",
        "mac",
        "windows"
      ]
    },
    {
      "slug": "megan.prelinger",
      "name": "Megan Prelinger",
      "url": "http://usesthis.com/interviews/megan.prelinger/",
      "summary": "Writer, historian, librarian, naturalist",
      "date": 1458025200,
      "categories": [
        "historian",
        "librarian",
        "mac",
        "naturalist",
        "writer"
      ],
      "credits": {
        "name": "Rick Prelinger (© 2014)"
      }
    }
  ]
}
```

| Element     |   Description   |   Type   |   Notes   |
|-------------|-----------------|----------|-----------|
|  **interviews**  |  Basic interview information   |   JSON array   |  |
|  **{interviews}/slug**  |    Page ID    |  string   |  In "first.last" name format    |
|  **{interviews}/name**  |    Full name  |  string   |  First and last name    |
|  **{interviews}/url**  |    Link to full interview        |  string   |  |
|  **{interviews}/summary**  |    Summary of the interview        |  string   |  |
|  **{interviews}/date**  |    Date interview was posted  |  integer   |  **date** is in UNIX epoch time    |
|  **{interviews}/categories**  |    List of categories for the interview  |  JSON array   |  |
|  **{interviews}/credits**  |    Photo credit for interview picture    |  JSON object   |  Credit is only listed when provided by subject    |
|  **{interviews}/{credits}/name**  |    Name of photographer        |  string   |  &nbsp;    |

### Status Codes and Errors

|     Code    | Description     |  Notes       |
|-------------|-----------------|--------------|
|  **200**    |    OK           |  Success     |
|  **404**    |    Not found    |  API endpoint not found |

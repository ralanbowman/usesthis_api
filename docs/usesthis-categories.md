## Retrieve a list of all interviews in a category

Returns a list of all interviews available in a specified category.

### Endpoint

`/api/v1/categories/{slug}`

**Note** - a ***slug*** is a short label for a category that is used as part of a URL. See **Retrieve a list of all categories** to get a full list of available slugs.

### Method and URL

`GET https://usesthis.com/api/v1/categories/{slug}`


### Sample Request

`curl -X GET "https://usesthis.com/api/v1/categories/mac/"`


### Sample Response

```json
{
  "interviews": [
    {
      "slug": "first.last",
      "name": "Firstname Lastname",
      "url": "http://usesthis.com/interviews/slug.name/",
      "summary": "Summary of interview subject",
      "date": 1410962400,
      "categories": [
        "category1",
        "category2",
        "category3",
        "category4"
      ]
    }
  ]
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

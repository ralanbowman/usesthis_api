## Retrieve a list of all categories

Returns a basic list of all categories currently available

**Note** - this will return a long list of items.

### Endpoint

`/api/v1/categories`

### Method and URL

`GET https://usesthis.com/api/v1/categories`


### Sample Request

`curl -X GET "https://usesthis.com/api/v1/categories/"`


### Sample Response

```json
{
  "categories": [
    "activist",
    "actor",
    "adventurer",
    "agriculture",
    "animal",
    "animator",
    "anthropologist",
    "architect",
    "artist",
    "astrologer",
    "output truncated..."
   ]
}
```


| Element     |   Description   |   Type   |   Notes   |
|-------------|-----------------|----------|-----------|
|  **categories**  |    List of categories        |  JSON array   |  &nbsp;    |

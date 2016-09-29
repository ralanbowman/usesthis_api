## Retrieve site stats for number of interviews, hardware and software item counts

Returns a count of the current number of interviews posted, and the number of hardware and software items counted. 

**Note** - these numbers will change as the site is updated. 

### Endpoint

`/api/v1/stats`

### Method and URL

`GET https://usesthis.com/api/v1/stats/`


### Sample Request

`curl -X GET https://usesthis.com/api/v1/stats/`


### Sample Response

```json
{
  "interviews": 708,
  "hardware": 2583,
  "software": 3029
}
```


| Element     |   Description   |   Type   |   Notes   |
|-------------|-----------------|----------|-----------|
|  **interviews**  | Current number of interviews   |  integer   |  &nbsp;    |
|  **hardware**  |    Current number of hardware items counted   |  integer   |  &nbsp;    |
|  **software**  |    Current number of software items counted   |  integer   |  &nbsp;    |



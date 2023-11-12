# API: List Aggregators

### Use Cases
Use this endpoint to list all aggregators in the system.

### URL
```
GET {baseUrl}/admin/aggregators/?search=times&page=1&page_size=10
```
| Parameter | Type | Description                   |
|-----------|------|-------------------------------|
| search    | str  | The search query              |
| page_size | int  | The no. of contents in a page |
| page      | int  | The current page              |


### Headers
```
Authorization: Bearer {jwt_token}
```

### Response Format
The API will return a `200 OK` with the below response body.

```
{
    count: 239,
    "next": "{baseUrl}/admin/aggregators/?search=times&page=2&page_size=10"
    "previous": null,
    "results": [
        {
            "name": "Times of India",
            "apis": {
                "today_api_url": "https://timesofindia.com/api/news/today/",
                "headlines_api_url": "https://timesofindia.com/api/news/headlines/",
                "international_api_url": "https://timesofindia.com/api/news/international/"
            },
            "data_update_frequency_in_mins": 60  
        }
    ]
}
```


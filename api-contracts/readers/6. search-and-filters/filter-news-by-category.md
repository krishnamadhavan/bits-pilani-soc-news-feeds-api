# API: Filter News Feeds by Category

### Use Cases
Use this endpoint to filter news feeds by category and sort them by date. 

### URL
```
POST {baseUrl}/news/filtering/?ordering=updated_at&page=&page_size=
```
| Parameter | Type | Description                                      |
|-----------|------|--------------------------------------------------|
| ordering  | str  | Possible values are `updated_at` & `-updated_at` |
| page      | int  | The current page                                 |
| page_size | int  | The no. of contents in a page                    |


### Headers
```
Content-Type: application/json
Authorization: Bearer {jwt_token}
```

### Request Payload
{
    "slugs": [
        "the-rise-of-covid-19",
        "the-advent-of-nipah-virus",
    ]
}

### Response Format
The API will return a `200 OK` with the below response body.

```
{
    count: 85,
    "next": "{baseUrl}/filtering/?ordering=updated_at&page=&page_size=
    "previous": null,
    "results": [
        {
            "slug": "the-rise-of-covid-19",
            "title": "The rise of COVID-19 infection.",
            "short_description": "Coronavirus disease (COVID-19) is an infectious disease caused by the SARS-CoV-2 virus.",
            "image_url": "https://example.com/the-rise-of-covid-19.png",
            "external_news_url": "https://timesofindia.com/the-rise-of-covid-19",
            "category": {
                "slug": "medicine",
                "name": "Medicine"
            }            
        }
    ]
}
```


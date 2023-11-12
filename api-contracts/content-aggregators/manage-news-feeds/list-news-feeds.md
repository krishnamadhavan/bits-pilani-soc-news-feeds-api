# API: List News Feeds curated from Aggregators

### Use Cases
Use this endpoint to list the news feeds based curated from the aggregators.

### URL
```
GET {baseUrl}/admin/news/?search=covid&page=1&page_size=10
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
    count: 87685,
    "next": "{baseUrl}/admin/news/?search=covid&page=2&page_size=10"
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
            },
            "aggregator": {
                "name": "Times of India"
            },
            "is_published": true
        }
    ]
}
```


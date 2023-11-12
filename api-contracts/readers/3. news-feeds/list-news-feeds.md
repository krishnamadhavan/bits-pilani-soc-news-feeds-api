# API: List News Feeds

### Use Cases
Use this endpoint to list a continuous feed of news based on user's selected preferences.

### URL
```
GET {baseUrl}/news/personalized/?page=&page_size=
```
| Parameter | Type | Description                   |
|-----------|------|-------------------------------|
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
    "next": "{baseUrl}/news/personalized/?page=2"
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


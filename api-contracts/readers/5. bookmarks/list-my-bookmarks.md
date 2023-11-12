# API: List my Bookmarks

### Use Cases
Use this endpoint to list my bookmarks of news-feeds

### URL
```
GET {baseUrl}/bookmarks/
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
The API will return a `200 OK` with the below format.

```
{
    count: 24,
    "next": "{baseUrl}/bookmarks/?page=2"
    "previous": null,
    "results": [
        {
            "slug": "the-rise-of-covid-19",
            "title": "The rise of COVID-19 infection.",
            "short_description": "Coronavirus disease (COVID-19) is an infectious disease caused by the SARS-CoV-2 virus.",
            "image_url": "https://example.com/the-rise-of-covid-19.png",
            "category": {
                "slug": "medicine",
                "name": "Medicine"
            }
        }
    ]
}
```
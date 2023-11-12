# API: Add Aggregator to the Platform

### Use Cases
Use this endpoint to add an aggregator to the platform.

### URL
```
POST {baseUrl}/admin/aggregators/
```

### Headers
```
Content-Type: application/json
Authorization: Bearer {jwt_token}
```

### Request Payload
```
{
    "name": "Times of India",
    "apis": {
        "today_api_url": "https://timesofindia.com/api/news/today/",
        "headlines_api_url": "https://timesofindia.com/api/news/headlines/",
        "international_api_url": "https://timesofindia.com/api/news/international/"
    },
    "data_update_frequency_in_mins": 60  
}
```

### Response Format
Upon successful creation, the API will return a `201 Created` with the below response body.

# API: Create a Bookmark

### Use Cases
Use this endpoint to bookmark a news-feed

### URL
```
POST {baseUrl}/bookmarks/
```

### Headers
```
Content-Type: application/json
Authorization: Bearer {jwt_token}
```

### Request Payload
```
{
    "slug": "the-rise-of-covid-19"
}
```

### Response Format
Upon successful registration, the API will return a `201 Created`.

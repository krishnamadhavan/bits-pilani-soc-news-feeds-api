# API: Retrieve UserProfile

### Use Cases
Use this endpoint to retrieve a user's profile & preferences

### URL
```
GET {baseUrl}/users/me/
```

### Headers
```
Authorization: Bearer {jwt_token}
```

### Response Format
The API will return a `200 OK` with the below response body.

```
{
    "first_name": "Krishna",
    "last_name": "Madhavan",
    "username": "madhavank",
    "email": "krishnamadhavan07@gmail.com",
    "preferences": {
        "language": "en",
        "sources": [
            {
                "url": "https://timesofindia.com",
                "name": "Times of India"
            }
        ],
        "categories": [
            {
                "slug": "business",
                "name": "Business"
            }
        ]
    }
}
```

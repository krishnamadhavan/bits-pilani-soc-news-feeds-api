# API: Update UserProfile

### Use Cases
Use this endpoint to update a user's profile & preferences

### URL
```
PATCH {baseUrl}/users/me/
```

### Headers
```
Content-Type: application/json
Authorization: Bearer {jwt_token}
```

### Request Payload
All the fields in this payload are optional, this allows the client to send only the parameters that are updated.
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
                "name": "Times of India",
                "slug": "times_of_india"
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
                "name": "Times of India",
                "slug": "times_of_india"
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

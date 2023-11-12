# API: User Registration

### Use Cases
Use this endpoint to register a user

### URL
```
POST {baseUrl}/oauth2/register/
```

### Headers
```
Content-Type: application/json
```

### Request Payload
```
{
    "username": "madhavank",
    "email": "krishnamadhavan07@gmail.com",
    "first_name": "Krishna",
    "last_name": "Madhavan",
    "password": "user@123"
}
```

### Response Format
Upon successful registration, the API will return a `201 Created`.

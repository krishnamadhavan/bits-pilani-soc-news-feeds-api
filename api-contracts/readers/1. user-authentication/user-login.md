# API: User Login

### Use Cases
Use this endpoint to login a user

### URL
```
POST {baseUrl}/oauth2/login/
```

### Headers
```
Content-Type: application/json
```

### Request Payload
```
{
    "username": "madhavank",
    "password": "user@123"
}
```

### Response Format
Upon successful login, the API will return a `200 OK` with the below response body.

```
{
    "access_token": "eyJraWQ.....rm8EA4osYg",
    "refresh_token": "i6mapTIAVSp2oJkgUnCACKKfZxt_H5MBLiqcybBBd04",
    "expires_in": 3600,
    "token_type": "Bearer"
}
```

If the username or password is invalid, then the API returns a `400 Bad Request`.

```
{
    "non_field_errors": "The username or password is incorrect."
}
```

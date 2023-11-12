# API: Publish or Unpublish a News Feed

### Use Cases
Use this endpoint to publish or unpublish a news feed.

### URL
```
PATCH {baseUrl}/admin/news/{slug}/
```
| Parameter | Type | Description                 |
|-----------|------|-----------------------------|
| slug      | str  | The unique slug of the news |

### Headers
```
Content-Type: application/json
Authorization: Bearer {jwt_token}
```

### Request Payload
```
{
    "is_published": true
}

The possible options are: `true` and `false`. 
```

### Response Format
Upon successful status change, the API will return a `200 OK`.

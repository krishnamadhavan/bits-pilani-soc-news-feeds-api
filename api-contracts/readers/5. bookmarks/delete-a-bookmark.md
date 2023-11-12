# API: Delete a Bookmark

### Use Cases
Use this endpoint to delete a bookmarked news-feed

### URL
```
DELETE {baseUrl}/bookmarks/{id}/
```
| Parameter | Type | Description                   |
|-----------|------|-------------------------------|
| id        | int  | The unique ID of the bookmark |

### Headers
```
Authorization: Bearer {jwt_token}
```

### Response Format
Upon successful deletion, the API will return a `204 No Content`.

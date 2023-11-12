# API: Admin Dashboard View

### Use Cases
Use this endpoint to view necessary details for the Admin Dashboard.

### URL
```
GET {baseUrl}/admin/dashboard/
```

### Headers
```
Authorization: Bearer {jwt_token}
```

### Response Format
The API will return a `200 OK` with the below response body.

```
{
    "total_news_num": 987324,
    "news_added_today_num": 809,
    "total_users_num": 23094,
    "users_registred_today_num": 2130,
    "average_usage_time_in_mins": 28,
}
```

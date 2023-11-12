# API: Enable or Disable an Aggregator

### Use Cases
Use this endpoint to enable or disable an aggregator in the platform.

### URL
```
PATCH {baseUrl}/admin/aggregators/{id}/
```
| Parameter | Type | Description                     |
|-----------|------|---------------------------------|
| id        | int  | The unique ID of the aggregator |

### Headers
```
Content-Type: application/json
Authorization: Bearer {jwt_token}
```

### Request Payload
```
{
    "is_enabled": true
}

The possible options are: `true` and `false`. 
```

### Response Format
Upon successful status change, the API will return a `200 OK`.

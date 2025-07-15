```markdown
# Get All Users

Retrieve a list of all registered users.

---

## Endpoint

**GET** `/api/users`

## Headers

| Key            | Value                     |
|----------------|---------------------------|
| Authorization  | Bearer YOUR_API_KEY       |
| Content-Type   | application/json          |

## Query Parameters

| Name   | Type | Required | Description                             |
|--------|------|----------|-----------------------------------------|
| page   | int  | No       | Page number for pagination              |
| limit  | int  | No       | Number of users per page (default: 20)  |

---

## Example Request

```http
GET /api/users?page=1&limit=10 HTTP/1.1
Host: api.tasktrack.com
Authorization: Bearer QpwL5tke4Pnpja7X4
```

---

## Success Response (200 OK)

```json
{
  "data": [
    {
      "id": 1,
      "name": "Jane Doe",
      "email": "jane@example.com"
    },
    {
      "id": 2,
      "name": "John Smith",
      "email": "john@example.com"
    }
  ]
}
```

---

## Error Response (401 Unauthorized)

```json
{
  "error": "Missing or invalid token"
}
```

---

## Notes

- Requires a valid Bearer token in the `Authorization` header.
- Pagination is optional but recommended for large datasets.
```

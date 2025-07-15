# Users API

## GET /api/users

Retrieve a list of all registered users.

---

### 🔹 HTTP Method & Endpoint

```
GET /api/users
```

### 🔹 Query Parameters

| Name  | Type   | Required | Description                             |
|-------|--------|----------|-----------------------------------------|
| page  | int    | No       | Page number for pagination              |
| limit | int    | No       | Number of users per page (default: 20) |

---

### 🔹 Example Request

```http
GET /api/users?page=1&limit=10 HTTP/1.1  
Host: api.tasktrack.com  
Authorization: Bearer YOUR_API_KEY
```

---

### 🔹 Response

**Status:** `200 OK`

```json
[
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
```

---

### 📘 Notes

- Requires a valid `Bearer token` in the `Authorization` header.
- Pagination is optional but recommended for large datasets.

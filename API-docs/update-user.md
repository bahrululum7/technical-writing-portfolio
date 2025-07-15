# Users API

## PUT /api/users/:id

Update an existing user's information by user ID.

---

### 🔹 HTTP Method & Endpoint

```
PUT /api/users/:id
```

- `:id` → Path parameter, ID dari user yang ingin diubah.

---

### 🔹 Request Body

Send JSON payload with the updated user data.

| Field    | Type   | Required | Description                    |
|----------|--------|----------|--------------------------------|
| name     | string | No       | Full name of the user          |
| email    | string | No       | New email address (must be unique) |
| password | string | No       | New password (plain-text)      |

📌 You can update one or more fields. Only include the fields you want to change.

---

### 🔹 Example Request

```http
PUT /api/users/101 HTTP/1.1  
Host: api.tasktrack.com  
Content-Type: application/json  
Authorization: Bearer YOUR_API_KEY

{
  "name": "Alice Johnson",
  "email": "alice.johnson@example.com"
}
```

---

### 🔹 Response

**Status:** `200 OK`

```json
{
  "id": 101,
  "name": "Alice Johnson",
  "email": "alice.johnson@example.com",
  "updated_at": "2025-07-15T09:45:00Z"
}
```

---

### 📘 Notes

- Authorization token is required.
- Only fields included in the request will be updated.
- Returns updated user object upon success.

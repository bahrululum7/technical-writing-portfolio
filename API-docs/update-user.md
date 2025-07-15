# Update User

Update an existing user's information by user ID.

---

## Endpoint

**PUT** `/api/users/:id`

- `:id` → Path parameter representing the user’s unique ID.

---

## Headers

| Key            | Value                     |
|----------------|---------------------------|
| Content-Type   | application/json          |
| Authorization  | Bearer YOUR_API_KEY       |

---

## Request Body

Send a JSON payload with the fields to update.

| Field    | Type   | Required | Description                          |
|----------|--------|----------|--------------------------------------|
| name     | string | No       | Full name of the user                |
| email    | string | No       | New email address (must be unique)   |
| password | string | No       | New password (plain-text)            |

📌 You can update one or more fields. Only include the fields you want to change.

---

## Example Request

```http
PUT /api/users/101 HTTP/1.1
Host: api.tasktrack.com
Content-Type: application/json
Authorization: Bearer QpwL5tke4Pnpja7X4

{
  "name": "Alice Johnson",
  "email": "alice.johnson@example.com"
}
```

---

## Success Response (200 OK)

```json
{
  "id": 101,
  "name": "Alice Johnson",
  "email": "alice.johnson@example.com",
  "updated_at": "2025-07-15T09:45:00Z"
}
```

---

## Error Responses

### 400 Bad Request

```json
{
  "error": "Invalid email format"
}
```

### 404 Not Found

```json
{
  "error": "User not found"
}
```

---

## Notes

- Authorization token is required.
- Only fields included in the request will be updated.
- Returns the updated user object upon success.
```

# Users API

## POST /api/users

Create a new user in the system.

---

### 🔹 HTTP Method & Endpoint

```
POST /api/users
```

### 🔹 Request Body

Send JSON payload in the request body.

| Field   | Type   | Required | Description         |
|---------|--------|----------|---------------------|
| name    | string | Yes      | Full name of user   |
| email   | string | Yes      | Email address       |
| password| string | Yes      | Plain-text password |

---

### 🔹 Example Request

```http
POST /api/users HTTP/1.1  
Host: api.tasktrack.com  
Content-Type: application/json  
Authorization: Bearer YOUR_API_KEY

{
  "name": "Alice Walker",
  "email": "alice@example.com",
  "password": "securepassword123"
}
```

---

### 🔹 Response

**Status:** `201 Created`

```json
{
  "id": 101,
  "name": "Alice Walker",
  "email": "alice@example.com",
  "created_at": "2025-07-15T08:30:00Z"
}
```

---

### 📘 Notes

- All fields are required.
- Email must be unique.
- Password will be securely hashed by the server.

# Create User

Create a new user in the system.

---

## Endpoint

**POST** `/api/users`

---

## Headers

| Key            | Value                     |
|----------------|---------------------------|
| Content-Type   | application/json          |
| Authorization  | Bearer YOUR_API_KEY       |

---

## Request Body

Send a JSON payload in the request body:

| Field    | Type   | Required | Description             |
|----------|--------|----------|-------------------------|
| name     | string | Yes      | Full name of the user   |
| email    | string | Yes      | Email address (unique)  |
| password | string | Yes      | Plain-text password     |

---

## Example Request

```http
POST /api/users HTTP/1.1
Host: api.tasktrack.com
Content-Type: application/json
Authorization: Bearer QpwL5tke4Pnpja7X4

{
  "name": "Alice Walker",
  "email": "alice@example.com",
  "password": "securepassword123"
}
```

---

## Success Response (201 Created)

**Headers:**

```http
Location: /api/users/101
```

**Body:**

```json
{
  "id": 101,
  "name": "Alice Walker",
  "email": "alice@example.com",
  "created_at": "2025-07-15T08:30:00Z"
}
```

---

## Error Response (400 Bad Request)

```json
{
  "error": "Email already exists"
}
```

---

## Notes

- All fields are required.
- Email must be unique.
- Password will be securely hashed on the server.
- A `Location` header will be included in the response pointing to the newly created resource.
```

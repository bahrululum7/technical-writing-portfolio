# Users API

## DELETE /api/users/:id

Delete an existing user by user ID.

---

### 🔹 HTTP Method & Endpoint

```
DELETE /api/users/:id
```

- `:id` → Path parameter untuk menentukan user mana yang ingin dihapus.

---

### 🔹 Example Request

```http
DELETE /api/users/101 HTTP/1.1  
Host: api.tasktrack.com  
Authorization: Bearer YOUR_API_KEY
```

---

### 🔹 Response

**Status:** `204 No Content`

(no response body)

---

### 📘 Notes

- Requires a valid authentication token.
- If the user does not exist, the server should return `404 Not Found`.
- `204 No Content` means the operation succeeded but there’s no data to return.

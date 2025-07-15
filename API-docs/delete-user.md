# Delete User

Delete an existing user by user ID.

---

## Endpoint

**DELETE** `/api/users/:id`

- `:id` → Path parameter for the unique user ID to be deleted.

---

## Headers

| Key            | Value               |
|----------------|---------------------|
| Authorization  | Bearer YOUR_API_KEY |

---

## Example Request

```http
DELETE /api/users/101 HTTP/1.1
Host: api.tasktrack.com
Authorization: Bearer QpwL5tke4Pnpja7X4
```

---

## Success Response (204 No Content)

- The user was successfully deleted.
- No content will be returned in the response body.

---

## Error Response (404 Not Found)

```json
{
  "error": "User not found"
}
```

---

## Notes

- Requires a valid authentication token.
- Returns `204 No Content` on successful deletion.
- If the user ID does not exist, returns `404 Not Found`.
```

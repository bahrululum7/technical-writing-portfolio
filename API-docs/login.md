# User Login

Authenticates a user and returns an access token.

---

## Endpoint

**POST** `/api/login`

---

## Headers

| Key           | Value              |
|---------------|--------------------|
| Content-Type  | application/json   |
| x-api-key     | reqres-free-v1     |

---

## Request Body

```json
{
  "email": "eve.holt@reqres.in",
  "password": "cityslicka"
}
```

---

## Success Response (200 OK)

```json
{
  "token": "QpwL5tke4Pnpja7X4"
}
```

---

## Error Responses

### 400 Bad Request

```json
{
  "error": "Missing email or password"
}
```

### 401 Unauthorized

```json
{
  "error": "Invalid credentials"
}
```

### 500 Internal Server Error

```json
{
  "error": "Unexpected server error"
}
```

---

## Notes

- Both `email` and `password` fields are required.
- The returned `token` is used to authenticate protected endpoints.
- No token will be returned if the login credentials are incorrect.

---

## Example in Postman

1. **Method:** POST  
2. **URL:** `https://reqres.in/api/login`  
3. **Headers:**
   - `Content-Type`: `application/json`
   - `x-api-key`: `reqres-free-v1`  
4. **Body (raw, JSON):**

```json
{
  "email": "eve.holt@reqres.in",
  "password": "cityslicka"
}
```
```

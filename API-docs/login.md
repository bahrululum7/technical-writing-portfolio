```markdown
# User Login

Authenticates a user and returns a login token.

## Endpoint

**POST** `/api/login`

## Headers

| Key           | Value              |
|---------------|--------------------|
| Content-Type  | application/json   |
| x-api-key     | reqres-free-v1     |

## Request Body

```json
{
  "email": "eve.holt@reqres.in",
  "password": "cityslicka"
}
```

## Success Response (200 OK)

```json
{
  "token": "QpwL5tke4Pnpja7X4"
}
```

## Error Responses

| Status Code | Description                     |
|-------------|---------------------------------|
| 400         | Missing email or password       |
| 401         | Invalid credentials             |
| 500         | Internal server error           |

## Notes

- Email and password are required fields.
- The token is used for accessing protected endpoints (if any).
- No token is returned if credentials are invalid.

## Example in Postman

1. Method: **POST**
2. URL: `https://reqres.in/api/login`
3. Headers:
   - `Content-Type`: `application/json`
   - `x-api-key`: `reqres-free-v1`
4. Body (raw, JSON):

```json
{
  "email": "eve.holt@reqres.in",
  "password": "cityslicka"
}
```
```

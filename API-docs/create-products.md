```markdown
# Create Product

Creates a new product in the system.

## Endpoint

**POST** `/api/products`

## Headers

| Key           | Value              |
|---------------|--------------------|
| Content-Type  | application/json   |
| x-api-key     | reqres-free-v1     |

## Request Body

```json
{
  "name": "Laptop X200",
  "price": 1499.99,
  "stock": 50
}
```

## Success Response (201 Created)

```json
{
  "id": "12345",
  "name": "Laptop X200",
  "price": 1499.99,
  "stock": 50,
  "createdAt": "2025-07-15T12:00:00Z"
}
```

## Error Responses

| Status Code | Description                 |
|-------------|-----------------------------|
| 400         | Invalid input data          |
| 401         | Missing or invalid API key  |
| 500         | Internal server error       |

## Notes

- The `name` field must be a non-empty string.
- The `price` must be a positive number.
- The `stock` must be an integer greater than or equal to 0.

## Example in Postman

1. Method: **POST**
2. URL: `https://reqres.in/api/products`
3. Headers:
   - `Content-Type`: `application/json`
   - `x-api-key`: `reqres-free-v1`
4. Body (raw, JSON):

```json
{
  "name": "Laptop X200",
  "price": 1499.99,
  "stock": 50
}
```
```

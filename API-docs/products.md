# Update Product

Updates the details of an existing product based on its unique identifier.

---

## Endpoint

**PUT** `/api/products/{id}`

- `{id}` is the unique product identifier.

---

## Headers

| Key            | Value                    |
|----------------|--------------------------|
| Authorization  | Bearer {access_token}    |
| x-api-key      | reqres-free-v1           |
| Content-Type   | application/json         |

---

## Path Parameters

| Parameter | Type   | Required | Description                          |
|-----------|--------|----------|--------------------------------------|
| id        | string | Yes      | ID of the product to update          |

---

## Request Body

```json
{
  "name": "Ultra Milk Full Cream",
  "price": 7500,
  "in_stock": true,
  "categories": ["beverages", "milk"],
  "description": "Premium sterilized milk for daily nutrition.",
  "discount": 10,
  "weight_gram": 250,
  "tags": ["best-seller", "promo"],
  "is_active": true
}
```

### Request Body Fields

| Field        | Type    | Required | Description                             |
|--------------|---------|----------|-----------------------------------------|
| name         | string  | Yes      | Product name                            |
| price        | number  | Yes      | Price in local currency (e.g., IDR)     |
| in_stock     | boolean | Yes      | Product availability status             |
| categories   | array   | Yes      | List of product categories              |
| description  | string  | No       | Full product description                |
| discount     | number  | No       | Discount percentage                     |
| weight_gram  | number  | No       | Product weight in grams                 |
| tags         | array   | No       | Searchable product tags                 |
| is_active    | boolean | Yes      | Whether the product is currently active |

---

## Success Response (200 OK)

```json
{
  "id": "p-904",
  "updatedAt": "2025-07-15T11:45:09.123Z"
}
```

| Field       | Type   | Description                       |
|-------------|--------|-----------------------------------|
| id          | string | ID of the updated product         |
| updatedAt   | string | ISO timestamp of the update       |

---

## Error Responses

### 400 Bad Request

```json
{
  "error": "Invalid product data"
}
```

### 404 Not Found

```json
{
  "error": "Product not found"
}
```

---

## Example HTTP Request

```http
PUT /api/products/p-904 HTTP/1.1
Host: api.example.com
Authorization: Bearer your-access-token
x-api-key: reqres-free-v1
Content-Type: application/json

{
  "name": "Ultra Milk Full Cream",
  "price": 7500,
  "in_stock": true,
  "categories": ["beverages", "milk"],
  "description": "Premium sterilized milk for daily nutrition.",
  "discount": 10,
  "weight_gram": 250,
  "tags": ["best-seller", "promo"],
  "is_active": true
}
```

---

## Notes

- Optional fields include `description`, `discount`, `weight_gram`, and `tags`.
- A valid product ID must exist; otherwise, a `404 Not Found` will be returned.
- This endpoint requires authentication with admin-level privileges.
```

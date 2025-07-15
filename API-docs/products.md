## PUT /api/products/{id}

Updates the details of an existing product based on its unique identifier.

---

### Request

- **Method:** `PUT`  
- **URL:** `https://api.example.com/products/{id}`

#### Headers

| Header           | Value                    | Required |
|------------------|--------------------------|----------|
| `x-api-key`      | `reqres-free-v1`         | ✅        |
| `Authorization`  | `Bearer {access_token}`  | ✅        |
| `Content-Type`   | `application/json`       | ✅        |

#### Path Parameters

| Parameter | Type   | Required | Description                             |
|-----------|--------|----------|-----------------------------------------|
| `id`      | string | ✅        | Unique identifier of the product to update |

---

### Request Body

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

#### Request Body Fields

| Field        | Type    | Required | Description                             |
|--------------|---------|----------|-----------------------------------------|
| name         | string  | ✅        | Product name                            |
| price        | number  | ✅        | Price in local currency (e.g., IDR)     |
| in_stock     | boolean | ✅        | Product availability status             |
| categories   | array   | ✅        | List of product categories              |
| description  | string  | ❌        | Full product description                |
| discount     | number  | ❌        | Discount percentage                     |
| weight_gram  | number  | ❌        | Product weight in grams                 |
| tags         | array   | ❌        | Searchable product tags                 |
| is_active    | boolean | ✅        | Whether the product is currently active |

---

### Response

- **Status:** `200 OK`

```json
{
  "id": "p-904",
  "updatedAt": "2025-07-15T11:45:09.123Z"
}
```

| Field       | Type   | Description                       |
|-------------|--------|-----------------------------------|
| `id`        | string | ID of the updated product         |
| `updatedAt` | string | ISO timestamp of the update       |

---

### Example HTTP Request

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

### Notes

- Fields such as `description`, `discount`, `weight_gram`, and `tags` are optional.
- The product must have a unique `id` that exists in the system; otherwise, a `404 Not Found` may be returned.
- This endpoint is restricted to authenticated users with admin-level privileges.

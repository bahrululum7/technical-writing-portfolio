```markdown
# Glossary

This glossary contains technical terms commonly used in REST API documentation.

---

## API (Application Programming Interface)

A set of rules that allows software programs to communicate with each other. REST API is one type of API that uses HTTP requests.

---

## Endpoint

A specific URL path where an API can be accessed. Each endpoint represents a specific resource or action.

**Example:** `/api/users` or `/api/products/123`

---

## Method (HTTP Method)

Defines the type of action to perform on a resource.

- `GET`: Retrieve data
- `POST`: Create new data
- `PUT`: Update existing data
- `DELETE`: Remove data

---

## Request

The data sent by the client (such as a web app or Postman) to the API server. It includes method, headers, and body.

---

## Response

The data sent back from the server to the client. It includes status code and response body.

---

## Request Body

The JSON payload sent in a `POST` or `PUT` request that contains the data to be created or updated.

---

## Header

Metadata included in the request or response. Common headers include `Content-Type` and `Authorization`.

---

## JSON (JavaScript Object Notation)

A lightweight data format used for data exchange between client and server. Most REST APIs use JSON.

---

## Token

A unique string returned after login that is used to identify and authorize the user in future requests.

---

## Status Code

A 3-digit code in the response that indicates the result of the request.

- `200 OK`: Success
- `201 Created`: Resource created
- `400 Bad Request`: Invalid input
- `401 Unauthorized`: Login or token missing/invalid
- `404 Not Found`: Resource not found
- `500 Internal Server Error`: Server-side error

---

## Authentication

The process of verifying user identity, usually by requiring login credentials and returning a token.

---

## Authorization

The process of checking if a user has permission to access a certain resource, usually using a token in the request header.
```

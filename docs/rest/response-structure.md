# Structure of REST API Response

## Status Code
- 200, 404, etc.

## Headers
- Meta-data of the response (Content-Type, etc.)

## Body
- Contents of the response (optional)

### Example
**Response:**
```json
HTTP/1.1 200 OK
Content-Type: application/json

[
  {
    "id": 1,
    "product": "Laptop",
    "quantity": 2,
    "price": 1200
  },
  {
    "id": 2,
    "product": "Phone",
    "quantity": 1,
    "price": 800
  }
]

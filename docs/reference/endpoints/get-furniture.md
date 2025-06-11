# GET /furniture

Returns a list of all furniture items stored in the database.

## Request Method
GET

## Endpoint
/furniture

## Parameters
None

## Example Request
```http
GET /furniture
```

## Example Response

```
[
  {
    "id": 1,
    "name": "Eames Lounge Chair",
    "style_id": 1,
    "material": "Plywood, leather"
  },
  {
    "id": 2,
    "name": "Reclaimed Wood Coffee Table",
    "style_id": 4,
    "material": "Reclaimed wood, iron pipes, wire"
  }
]
```

## Status Codes

* `200 OK` – Furniture list returned successfully

* `404 Not Found` – No furniture data found
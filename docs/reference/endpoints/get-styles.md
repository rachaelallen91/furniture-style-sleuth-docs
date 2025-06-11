# GET /styles

Returns a list of all furniture styles.

## Request Method
`GET`

## Endpoint
`/styles`

## Request Body
None

## Parameters
None

## Example Request

```http
GET /styles
```

## Example Response

``` 
[
  {
    "id": 1,
    "name": "Midcentury Modern",
    "era": "1945-1970",
    "description": "Clean lines, minimalist, focus on function"
  },
  {
    "id": 2,
    "name": "Victorian",
    "era": "1837-1901",
    "description": "Ornate details, rich fabrics, dark wood"
  }
]
```

## Status Codes

* `200 OK` – Styles returned successfully

* `404 Not Found` – No style data found
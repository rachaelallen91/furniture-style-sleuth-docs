# GET /furniture/{id}

Returns a specific furniture item by its ID.

## Request Method
`GET`

## Endpoint
`/furniture/{id}`

## Request Body
None

## Parameters

| Parameter | Type    | Description                                   |
|-----------|---------|-----------------------------------------------|
| `id`      | integer | **Required.** The ID of the furniture to retrieve. |

## Example Request

```http
GET /furniture/1
```

## Example Response

```
{
  "id": 1,
  "name": "Midcentury Modern",
  "era": "1945-1970",
  "description": "Clean lines, minimalist, focus on function"
}
```

## Status Codes

* `200 OK` – Style found

* `404 Not Found` – Style not found
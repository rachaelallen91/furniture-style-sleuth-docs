# GET /styles/{id}

Returns a specific style by its ID.

## Request Method
`GET`

## Endpoint
`/styles/{id}`

## Request Body
None

## Parameters

| Parameter | Type    | Description                            |
|-----------|---------|----------------------------------------|
| `id`      | integer | **Required.** The ID of the style to fetch. |

## Example Request

```http
GET /styles/1
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
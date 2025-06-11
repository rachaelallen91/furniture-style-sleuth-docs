# POST /furniture

Adds a new furniture item to the database.

All fields must be provided and must reference a valid existing style.

## Request Method
`POST`

## Endpoint
`/furniture`

## Request Body Example

```json
{
  "id": 5,
  "name": "Modern Bookshelf",
  "style_id": 3,
  "material": "Birch wood, steel"
}
```

## Parameters

| Parameter   | Type     | Description                                                  |
|-------------|----------|--------------------------------------------------------------|
| `id`        | integer  | **Required.** The unique ID for the new furniture item.      |
| `name`      | string   | **Required.** The name of the furniture item.                |
| `style_id`  | integer  | **Required.** The ID of the style associated with the item.  |
| `material`  | string   | **Required.** The materials used in the item.                |

## Status Codes

- `201 Created` – Furniture item successfully added  
- `400 Bad Request` – Invalid data or missing required fields  
- `409 Conflict` – Item with the same ID already exists  

# PUT /furniture

Replaces an existing furniture item with a new version. You must provide the full object, including all required fields.

Use this operation when you want to overwrite the entire furniture entry.

## Request Method
`PUT`

## Endpoint
`/furniture`

## Request Body Example

```json
{
  "id": 2,
  "name": "Reclaimed Wood Coffee Table",
  "style_id": 4,
  "material": "Reclaimed wood, iron pipes, wire"
}
```

## Parameters

| Parameter   | Type     | Description                                                                 |
|-------------|----------|-----------------------------------------------------------------------------|
| `id`        | integer  | **Required.** The ID of the furniture item to update.                       |
| `name`      | string   | **Required.** The updated name of the furniture item.                       |
| `style_id`  | integer  | **Required.** The style ID that links to an existing style.                 |
| `material`  | string   | **Required.** The material(s) used in the furniture item.                   |

## Status Codes

- `200 OK` – Furniture item updated successfully  
- `400 Bad Request` – Invalid or incomplete data  
- `404 Not Found` – No item found with that ID  

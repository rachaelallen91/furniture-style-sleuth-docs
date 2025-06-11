# PUT /styles

Replaces an existing style with a new version. You must provide the full object with all required fields.

Use this when you want to fully overwrite the existing style.

## Request Method
`PUT`

## Endpoint
`/styles`

## Request Body Example

```json
{
  "id": 1,
  "name": "Midcentury Modern",
  "era": "1945–1970",
  "description": "Minimalist, functional, and organic design elements."
}
```

## Parameters

| Parameter     | Type     | Description                                                              |
|---------------|----------|--------------------------------------------------------------------------|
| `id`          | integer  | **Required.** The ID of the style to update.                             |
| `name`        | string   | **Required.** The updated name of the style.                             |
| `era`         | string   | **Required.** The updated time period for the style.                     |
| `description` | string   | **Required.** The updated description of the style’s characteristics.    |

## Status Codes
- `200 OK` – Style updated successfully  
- `400 Bad Request` – Invalid or incomplete data  
- `404 Not Found` – No style found with that ID  

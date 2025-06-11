# POST /styles

Adds a new furniture style to the database.

All fields are required and must follow formatting conventions.

## Request Method
`POST`

## Endpoint
`/styles`

## Request Body Example

```json
{
  "id": 5,
  "name": "Bohemian",
  "era": "1970–present",
  "description": "Eclectic, free-spirited style with layered textures and patterns."
}
```

## Parameters

| Parameter     | Type     | Description                                                    |
|---------------|----------|----------------------------------------------------------------|
| `id`          | integer  | **Required.** The unique ID for the new style.                 |
| `name`        | string   | **Required.** The name of the style.                           |
| `era`         | string   | **Required.** The time period associated with the style.       |
| `description` | string   | **Required.** A brief description of the style characteristics.|

## Status Codes

- `201 Created` – Style successfully added  
- `400 Bad Request` – Invalid or missing fields  
- `409 Conflict` – Style with the same ID already exists  

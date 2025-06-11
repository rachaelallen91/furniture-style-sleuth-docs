# PATCH /styles

This endpoint allows you to partially update an existing style.

Unlike `PUT`, which replaces the entire style object, `PATCH` lets you send only the fields you want to update. Fields not included in the request remain unchanged.

## Request Method
`PATCH`

## Endpoint
`/styles`

## Request Body Example

```json
{
  "id": 1,
  "description": "Clean lines, minimalist design, and a strong focus on functionality, often incorporating organic and geometric forms."
}
```

## Parameters

| Parameter     | Type     | Description                                                                                         |
|---------------|----------|-----------------------------------------------------------------------------------------------------|
| `id`          | integer  | **Required.** The unique identifier of the style to update.                                         |
| `name`        | string   | The updated name of the style.                                                                      |
| `era`         | string   | The updated era or period associated with the style.                                                |
| `description` | string   | The updated description of the style.                                                               |

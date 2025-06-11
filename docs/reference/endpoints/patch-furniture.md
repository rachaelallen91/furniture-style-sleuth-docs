# PATCH /furniture

This endpoint allows you to partially update an existing furniture item.

Unlike `PUT`, which replaces the entire item, `PATCH` lets you send only the fields you want to update.

## Request Method
`PATCH`

## Endpoint
`/furniture`

## Request Body Example

```json
{
  "id": 1,
  "name": "Eames Lounge Chair and Ottoman",
  "material": "Molded plywood, leather"
}
```
## Parameters

| Parameter    | Type     | Description                                                                                         |
|--------------|----------|-----------------------------------------------------------------------------------------------------|
| `id`         | integer  | **Required.** The unique identifier of the style to update.                                         |
| `name`       | string   | The updated name of the style.                                                                      |
| `era`        | string   | The updated era or period associated with the style.                                                |
| `description`| string   | The updated description of the style.                                                               |

# Reference: PATCH Endpoints

This page documents the PATCH methods available in the Furniture Style Sleuth API. These endpoints allow you to update specific fields of existing resources without replacing the entire object.

## PATCH /furniture

This endpoint allows you to partially update an existing furniture item.

Unlike `PUT`, which replaces the entire item, `PATCH` lets you send only the fields you want to update.

**Request Method:** `PATCH`

**Endpoint:** `/furniture`

### Request Body Example

```json
{
  "id": 1,
  "name": "Eames Lounge Chair and Ottoman",
  "material": "Molded plywood, leather"
}
```

### Parameters

| Parameter    | Type     | Description                                                                                         |
|--------------|----------|-----------------------------------------------------------------------------------------------------|
| `id`         | integer  | **Required.** The unique identifier of the style to update.                                         |
| `name`       | string   | The updated name of the style.                                                                      |
| `material`        | string   | Updated list of materials (comma-separated).                                                |
| `style_id`| integer   | ID of the associated style.  |

---

## PATCH /styles

This endpoint allows you to partially update an existing style.

Unlike `PUT`, which replaces the entire style object, `PATCH` lets you send only the fields you want to update. Fields not included in the request remain unchanged.

**Request Method:** `PATCH`

**Endpoint:** `/styles`

### Request Body Example

```json
{
  "id": 1,
  "description": "Clean lines, minimalist design, and a strong focus on functionality, often incorporating organic and geometric forms."
}
```

### Parameters

| Parameter     | Type     | Description                                                                                         |
|---------------|----------|-----------------------------------------------------------------------------------------------------|
| `id`          | integer  | **Required.** The unique identifier of the style to update.                                         |
| `name`        | string   | The updated name of the style.                                                                      |
| `era`         | string   | The updated era or period associated with the style.                                                |
| `description` | string   | The updated description of the style.                                                               |

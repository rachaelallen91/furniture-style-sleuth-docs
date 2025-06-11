# DELETE /styles/{id}

Deletes a furniture style by its ID.

This operation removes the style and may impact any furniture items associated with this style. Use with caution.

## Request Method
`DELETE`

## Endpoint
`/styles/{id}`

## Request Body
None

## Parameters

| Parameter | Type    | Description                            |
|-----------|---------|----------------------------------------|
| `id`      | integer | **Required.** The ID of the style to delete. |

## Example Request

```http
DELETE /styles/4
```

## Status Codes

`204 No Content` – Style deleted successfully

`404 Not Found` – No style found with that ID

`400 Bad Request` – Style is linked to existing furniture items
# DELETE /furniture/{id}

Deletes a furniture item by its ID.

This operation permanently removes the furniture item from the database.

## Request Method
`DELETE`

## Endpoint
`/furniture/{id}`

## Request Body
None

## Parameters

| Parameter | Type    | Description                                  |
|-----------|---------|----------------------------------------------|
| `id`      | integer | **Required.** The ID of the furniture item to delete. |

## Example Request

```http
DELETE /furniture/2
```

## Status Codes

`204 No Content` – Furniture item deleted successfully

`404 Not Found` – No item found with that ID
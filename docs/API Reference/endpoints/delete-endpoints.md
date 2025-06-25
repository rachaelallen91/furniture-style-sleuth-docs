# Reference: DELETE Endpoints

This page documents the DELETE methods available in the Furniture Style Sleuth API. These endpoints allow you to remove furniture items or styles from the database.

## DELETE /furniture/{id}

Deletes a furniture item by its ID.

This operation permanently removes the furniture item from the database.

**Request Method:** `DELETE`

**Endpoint:** `/furniture/{id}`

### Request Body
None

### Parameters

| Parameter | Type    | Description                                  |
|-----------|---------|----------------------------------------------|
| `id`      | integer | **Required.** The ID of the furniture item to delete. |

### Example Request

```http
DELETE /furniture/2
```

### Status Codes

`204 No Content` – Furniture item deleted successfully

`404 Not Found` – No item found with that ID


## DELETE /styles/{id}

Deletes a furniture style by its ID.

:::(warning)
Use with caution: this operation may affect furniture items that reference this style.
:::

**Request Method:** `DELETE`

**Endpoint:** `/styles/{id}`

### Request Body
None

### Parameters

| Parameter | Type    | Description                            |
|-----------|---------|----------------------------------------|
| `id`      | integer | **Required.** The ID of the style to delete. |

### Example Request

```http
DELETE /styles/4
```

### Status Codes

`204 No Content` – Style deleted successfully

`404 Not Found` – No style found with that ID

`400 Bad Request` – Style is linked to existing furniture items
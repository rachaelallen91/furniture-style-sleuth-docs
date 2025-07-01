---
title: POST
nav_order: 2
parent: Endpoints
grand_parent: API Reference
---

# Reference: POST endpoints

This page documents the POST methods available in the Furniture Style Sleuth API. These endpoints allow you to add new furniture items or styles to the database.

## POST /furniture

Adds a new furniture item to the database.

All fields must be provided and must reference a valid existing style.

**Request Method:** `POST`

**Endpoint:** `/furniture`

### Request body example

```json
{
  "name": "Modern Bookshelf",
  "style_id": 3,
  "material": "Birch wood, steel"
}
```

### Parameters

| Parameter   | Type     | Description                                                  |
|-------------|----------|--------------------------------------------------------------|
| `name`      | string   | **Required.** The name of the furniture item.                |
| `style_id`  | integer  | **Required.** The ID of the style associated with the item.  |
| `material`  | string   | **Required.** The materials used in the item.                |

### Status codes

- `201 Created` – Furniture item successfully added  
- `400 Bad Request` – Invalid data or missing required fields  
- `409 Conflict` – Item with the same ID already exists  


## POST /styles

Adds a new furniture style to the database.

All fields are required and must follow formatting conventions.

**Request Method:** `POST`

**Endpoint:** `/styles`

### Request body example

```json
{
  "name": "Bohemian",
  "era": "1970–present",
  "description": "Eclectic, free-spirited style with layered textures and patterns."
}
```

### Parameters

| Parameter     | Type     | Description                                                    |
|---------------|----------|----------------------------------------------------------------|
| `name`        | string   | **Required.** The name of the style.                           |
| `era`         | string   | **Required.** The time period associated with the style.       |
| `description` | string   | **Required.** A brief description of the style characteristics.|

### Status codes

- `201 Created` – Style successfully added  
- `400 Bad Request` – Invalid or missing fields  
- `409 Conflict` – Style with the same ID already exists  

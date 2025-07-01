---
title: PUT
nav_order: 3
parent: Endpoints
grand_parent: API Reference
---


# Reference: PUT Endpoints

This page documents the PUT methods available in the Furniture Style Sleuth API. These endpoints allow you to replace entire records for furniture items or styles.

## PUT /furniture

Replaces an existing furniture item with a new version. You must provide the full object, including all required fields.

Use this operation when you want to overwrite the entire furniture entry.

**Request Method:** `PUT`

**Endpoint:** `/furniture`

### Request Body Example

```json
{
  "id": 2,
  "name": "Reclaimed Wood Coffee Table",
  "style_id": 4,
  "material": "Reclaimed wood, iron pipes, wire"
}
```

### Parameters

| Parameter   | Type     | Description                                                                 |
|-------------|----------|-----------------------------------------------------------------------------|
| `id`        | integer  | **Required.** The ID of the furniture item to update.                       |
| `name`      | string   | **Required.** The updated name of the furniture item.                       |
| `style_id`  | integer  | **Required.** The style ID that links to an existing style.                 |
| `material`  | string   | **Required.** The materials used to construct the furniture item.                   |

### Status Codes

- `200 OK` – Furniture item updated successfully  
- `400 Bad Request` – Invalid or incomplete data  
- `404 Not Found` – No item found with that ID  

## PUT /styles

Replaces an existing style with a new version. You must provide the full object with all required fields.

Use this when you want to fully overwrite the existing style.

**Request Method:** `PUT`

**Endpoint:** `/styles`

### Request Body Example

```json
{
  "id": 1,
  "name": "Midcentury Modern",
  "era": "1945–1970",
  "description": "Minimalist, functional, and organic design elements."
}
```

### Parameters

| Parameter     | Type     | Description                                                              |
|---------------|----------|--------------------------------------------------------------------------|
| `id`          | integer  | **Required.** The ID of the style to update.                             |
| `name`        | string   | **Required.** The updated name of the style.                             |
| `era`         | string   | **Required.** The updated time period for the style.                     |
| `description` | string   | **Required.** A description of the style's characteristics.    |

### Status Codes
- `200 OK` – Style updated successfully  
- `400 Bad Request` – Invalid or incomplete data  
- `404 Not Found` – No style found with that ID  

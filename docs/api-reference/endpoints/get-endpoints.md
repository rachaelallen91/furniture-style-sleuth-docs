---
title: GET
nav_order: 1
parent: Endpoints
grand_parent: API Reference
---

# Reference: GET endpoints

This page documents the GET methods available in the Furniture Style Sleuth API. These endpoints allow you to retrieve furniture items and styles.

## GET /furniture/{id}

Returns a specific furniture item by its ID.

**Request Method:** `GET`

**Endpoint:** `/furniture/{id}`

### Request body
None

### Parameters

| Parameter | Type    | Description                                   |
|-----------|---------|-----------------------------------------------|
| `id`      | integer | **Required.** The ID of the furniture to retrieve. |

### Example request

```http
GET /furniture/1
```

### Example response

```
{
  "id": 1,
  "name": "Eames Lounge Chair",
  "style_id": 1,
  "material": "Plywood, leather"
}
```

### Status codes

* `200 OK` – Style found

* `404 Not Found` – Style not found


## GET /furniture

Returns a list of all furniture items stored in the database.

**Request Method:** `GET`

**Endpoint:** `/furniture`

### Parameters
None

### Example request

```http
GET /furniture
```

### Example response

```
[
  {
    "id": 1,
    "name": "Eames Lounge Chair",
    "style_id": 1,
    "material": "Plywood, leather"
  },
  {
    "id": 2,
    "name": "Reclaimed Wood Coffee Table",
    "style_id": 4,
    "material": "Reclaimed wood, iron pipes, wire"
  }
]
```

### Status codes

* `200 OK` – Furniture list returned successfully

* `404 Not Found` – No furniture data found


## GET /styles/{id}

Returns a specific style by its ID.

**Request Method:** `GET`

**Endpoint:** `/styles/{id}`

### Request body
None

### Parameters

| Parameter | Type    | Description                            |
|-----------|---------|----------------------------------------|
| `id`      | integer | **Required.** The ID of the style to fetch. |

### Example request

```http
GET /styles/1
```

### Example response

```
{
  "id": 1,
  "name": "Midcentury Modern",
  "era": "1945-1970",
  "description": "Clean lines, minimalist, focus on function"
}
```

### Status codes

* `200 OK` – Style found

* `404 Not Found` – Style not found


## GET /styles

Returns a list of all furniture styles.

**Request method:** `GET`

**Endpoint:** `/styles`

### Request body
None

### Parameters
None

### Example request

```http
GET /styles
```

### Example response

``` 
[
  {
    "id": 1,
    "name": "Midcentury Modern",
    "era": "1945-1970",
    "description": "Clean lines, minimalist, focus on function"
  },
  {
    "id": 2,
    "name": "Victorian",
    "era": "1837-1901",
    "description": "Ornate details, rich fabrics, dark wood"
  }
]
```

### Status codes

* `200 OK` – Styles returned successfully

* `404 Not Found` – No style data found
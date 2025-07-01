---
title: Quickstart
nav_order: 1
---


# Quick start guide

Get up and running with the *Furniture Style Sleuth API* in just a few steps.

## 1. Overview

This API enables you to retrieve, add, and manage furniture items and design styles. It’s great for developers building search filters or educational tools around furniture aesthetics.

This API does not require authentication. You can start making calls right away.

## 2. Make your first API call

Use this endpoint to get a list of all furniture styles:

```http
GET /styles
```

### Example response

```json
[
  {
    "id": 1,
    "name": "Midcentury Modern",
    "era": "1945–1970",
    "description": "Clean lines, minimalist, focus on function"
  },
  {
    "id": 2,
    "name": "Victorian",
    "era": "1837–1901",
    "description": "Ornate details, rich fabrics, dark wood"
  },
  ...
]
```

## 3. Filter furniture by style

Once you know the style ID you want to filter by, use the following endpoint:

```http
GET /furniture?style_id=1
``` 

This request returns a list of furniture items in the selected style.

### Example response

```
[
  {
    "id": 1,
    "name": "Eames Lounge Chair",
    "style_id": 1,
    "material": "Plywood, leather"
  }
]
```

## 4. What’s next

- [Try a tutorial](tutorials/tutorial-find-furniture-by-style.md)
- [Explore all endpoints](topic-list.md)
- [View the reference for styles](api-reference/styles.md)
---
title: Add Furniture
nav_order: 2
parent: Tutorials
---


# Tutorial: Adding a new furniture item

This tutorial walks you through how to add a new furniture item using the `POST /furniture` endpoint.

## Step 1: Understand the required fields

To create a new item, you’ll need the following fields:

- `name`: The name of the furniture item
- `style_id`: The associated style ID
- `material`: A comma-separated string of materials

## Step 2: Send the request

Use this JSON in your `POST` request to `/furniture`:

```json
{
  "name": "Vintage Coffee Table",
  "style_id": 2,
  "material": "Oak, brass"
}
```

## Step 3: Check the response

A successful request returns a `201 Created` status and the new item:

```
{
  "id": 5,
  "name": "Vintage Coffee Table",
  "style_id": 2,
  "material": "Oak, brass"
}
```

## Step 4: Verify the addition

Use `GET /furniture` to confirm the item appears in the list.


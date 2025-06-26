---
title: Add Furniture
parent: Tutorials
grand_parent: Overview
nav_order: 3
---


# Tutorial: Adding a New Furniture Item

This tutorial walks you through how to add a new furniture item using the `POST /furniture` endpoint.

## Step 1: Understand the Required Fields

To create a new item, you’ll need the following fields:

- `name`: The name of the furniture item
- `style_id`: The associated style ID
- `material`: A comma-separated string of materials

## Step 2: Send the Request

Use this JSON in your `POST` request to `/furniture`:

```json
{
  "name": "Vintage Coffee Table",
  "style_id": 2,
  "material": "Oak, brass"
}
```

## Step 3: Check the Response

A successful request returns a `201 Created` status and the new item:

```
{
  "id": 5,
  "name": "Vintage Coffee Table",
  "style_id": 2,
  "material": "Oak, brass"
}
```

## Step 4: Verify the Addition

Use `GET /furniture` to confirm the item appears in the list.


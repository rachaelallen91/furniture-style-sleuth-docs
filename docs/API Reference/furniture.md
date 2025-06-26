---
title: Furniture
parent: API Reference
grand_parent: Overview
nav_order: 2
---


# Furniture resource

The `furniture` resource represents individual furniture items that can be categorized by design style.

## Data model

| Field     | Type   | Description |
|-----------|--------|-------------|
| `id`      | Integer | Unique identifier for the furniture item |
| `name`    | String  | Name of the furniture item |
| `style_id`| Integer | Foreign key that maps to a style (see styles resource) |
| `material`| String  | Comma-separated list of materials used (e.g. "Wood, Metal") |

## Example

```json
{
  "id": 2,
  "name": "Reclaimed Wood Coffee Table",
  "style_id": 4,
  "material": "Reclaimed wood, iron pipes, wire"
}

```

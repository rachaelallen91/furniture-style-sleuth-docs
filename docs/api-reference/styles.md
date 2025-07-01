---
title: Styles
nav_order: 2
parent: API Reference
---

# Styles resource

The `styles` resource represents design styles associated with furniture, including their name, historical era, and characteristics.

## Data model

| Field        | Type   | Description |
|--------------|--------|-------------|
| `id`         | Integer | Unique identifier for the style |
| `name`       | String  | Name of the style (e.g., "Midcentury Modern") |
| `era`        | String  | Historical period (e.g., "1945-1970") |
| `description`| String  | Key characteristics of the style |

## Example

```json
{
  "id": 1,
  "name": "Midcentury Modern",
  "era": "1945-1970",
  "description": "Clean lines, minimalist, focus on function"
}

```
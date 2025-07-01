---
title: Home
nav_order: 0
---



# Furniture style sleuth API

Welcome to the documentation for the **Furniture Style Sleuth API**—a lightweight RESTful service that helps developers identify furniture styles and build style-based furniture search features into their apps.

This API powers the Furniture Style Sleuth app, which enables users to upload a photo of a furniture item and learn its associated design style. With full support for two simple resources, it is easy to integrate into interior design tools, furniture discovery apps, or retail product filters.

Not sure where to begin? Start with the [Quick Start Guide](quickstart.md), or browse all available endpoints in the [API Overview](topic-list.md).


## What this API does

- Identify furniture by design style
- Look up style definitions by era and description
- Add, update, and remove furniture and style data
- Build search and filter features for example, "Show me all Industrial style items"

## Primary use cases

- Interior design apps that surface furniture style suggestions
- E-commerce platforms organizing products by aesthetic
- Developers building visual search tools for furniture
- Personal or educational tools for learning furniture history


## Available resources

The API includes two resources:

### Furniture
- Represents individual furniture items
- Fields: `id`, `name`, `style_id`, `material`
- Linked to a style via `style_id`

### Styles
- Represents historical or contemporary design styles
- Fields: `id`, `name`, `era`, `description`

## Endpoints

### Furniture endpoints

| Method | Endpoint            | Description                |
|--------|---------------------|----------------------------|
| GET    | `/furniture`        | List all furniture items   |
| GET    | `/furniture/{id}`   | Get a furniture item by ID |
| POST   | `/furniture`        | Add a furniture item       |
| PUT    | `/furniture/{id}`   | Replace a furniture item   |
| DELETE | `/furniture/{id}`   | Delete a furniture item    |

### Style endpoints

| Method | Endpoint          | Description              |
|--------|-------------------|--------------------------|
| GET    | `/styles`         | List all styles          |
| GET    | `/styles/{id}`    | Get a style by ID        |
| POST   | `/styles`         | Add a new style          |
| PUT    | `/styles/{id}`    | Update a style           |
| DELETE | `/styles/{id}`    | Delete a style           |

## Status codes

The API uses standard HTTP status codes, including:

- `200 OK` – Successful request
- `201 Created` – New resource created
- `204 No Content` – Successfully deleted
- `400 Bad Request` – Validation or formatting issue
- `404 Not Found` – Resource not found


## Authentication

Authentication is **not required** for this version of the API. It is open for educational and prototyping purposes.

## Explore the docs

- [Quick Start Guide](quickstart.md)
- [Tutorial: Finding Furniture by Style](tutorials/tutorial-find-furniture-by-style.md)
- [Furniture Overview](reference/furniture.md)
- [Styles Overview](reference/styles.md)
- [All Endpoints](topic-list.md)
- [Error Codes](errors.md)
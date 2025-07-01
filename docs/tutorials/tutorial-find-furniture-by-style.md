---
title: Find by Style
nav_order: 3
parent: Tutorials
---


# Tutorial: Finding Furniture by Style

This tutorial walks you through how to retrieve a list of furniture items based on a specific style using the Furniture Style Sleuth API.

## Scenario

You're designing a Midcentury Modern-themed room and want to find all furniture items that match that style. You’ll use the API to filter furniture by its associated style ID.

## Prerequisites

- A working internet connection
- Basic understanding of RESTful APIs
- Access to the Furniture Style Sleuth API
- A tool for making API requests (like Postman, curl, or your browser)

## Step 1: Look Up the Style ID

To filter furniture by style, you first need to know the style’s ID. Use the following endpoint to find it:

```http
GET /styles
```
### Example Response

```
[
  {
    "id": 1,
    "name": "Midcentury Modern",
    "era": "1945-1970",
    "description": "Clean lines, minimalist, focus on function"
  },
  {
    "id": 4,
    "name": "Industrial",
    "era": "1990-now",
    "description": "Raw materials, utilitarian design, exposed elements"
  }
]
```
From the response above, we see that the ID for **Midcentury Modern** is `1`.

## Step 2: Filter Furniture by Style

Use the following endpoint with a query parameter to find furniture items in that style:

```http
GET /furniture?style_id=1
```

### Example Response

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
## Step 3: Interpret the Results

The API returns a list of furniture items that match the specified style ID. Each object includes:

- `id`: Unique furniture identifier  
- `name`: Name of the item  
- `style_id`: Corresponding style  
- `material`: Materials used in the item  

In this example, you found an Eames Lounge Chair that fits the Midcentury Modern style.

## Summary

In this tutorial, you learned how to:

- Use the `/styles` endpoint to find a style ID  
- Use the `/furniture` endpoint to filter by that style  
- Interpret the filtered list of furniture items  

This is a helpful workflow for apps that let users shop or browse by design style.
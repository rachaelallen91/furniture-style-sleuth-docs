---
title: Quickstart
parent: Overview
nav_order: 2
---



# Quick Start Guide

Get up and running with the *Furniture Style Sleuth API* in just a few steps.

## 1. Overview

This API allows you to retrieve, add, and manage furniture items and design styles. It’s great for developers building search filters or educational tools around furniture aesthetics.

No authentication is required — you can start making calls right away.

## 2. Make Your First API Call

Use this endpoint to get a list of all furniture styles:

```http
GET /styles
```

### Example Response

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

## 3. Filter Furniture by Style

Once you know the style ID you want to filter by, use the following endpoint:

```http
GET /furniture?style_id=1
``` 

This request will return a list of furniture items in the selected style.

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

## 4. What’s Next?

- [Try a tutorial](tutorials/tutorial-find-furniture-by-style.md)
- [Explore all endpoints](topic-list.md)
- [View the reference for styles](reference/styles.md)
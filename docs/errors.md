---
title: Error Codes
nav_order: 3
---

# Error Codes

This page describes the standard HTTP status codes and error messages returned by the Furniture Style Sleuth API. Understanding these responses will help you troubleshoot issues during development.

## Common Status Codes

| Status Code | Meaning                | Description                                                                 |
|-------------|------------------------|-----------------------------------------------------------------------------|
| `200 OK`    | Success                | The request was successful and the response contains the expected data.    |
| `201 Created` | Resource Created     | The request was successful and a new resource was created.                 |
| `204 No Content` | Deleted           | The request was successful, but there is no content to return.            |
| `400 Bad Request` | Invalid Request  | The request was malformed or missing required fields.                      |
| `404 Not Found` | Resource Missing   | The requested resource could not be found.                                 |
| `409 Conflict` | Duplicate Entry     | The request conflicts with an existing resource (e.g., duplicate ID).      |
| `500 Internal Server Error` | Server Issue | An unexpected error occurred on the server.                          |

## Error Format

Error responses are returned in a consistent JSON structure:

```json
{
  "error": "Description of the error"
}
```

### Example

**Request:**

```http
GET /furniture/999
```

### Response 

```
{
  "error": "Furniture item not found"
}
```

## Tips for Debugging

If you encounter unexpected behavior when using the API, try the following:

- **Check your endpoint and method:** Make sure you're using the correct URL and HTTP method (`GET`, `POST`, `PUT`, `PATCH`, `DELETE`).
- **Verify required fields:** Double-check that your request includes all required parameters or JSON fields.
- **Inspect your JSON:** Ensure your request body is properly formatted. Use a linter or a tool like Postman to help.
- **Confirm the server is running:** The `json-server` service must be running in your terminal for the API to respond.
- **Review error messages:** The API returns helpful error messages. Use them to identify what went wrong.
- **Try a cURL or Postman request:** Sometimes tools provide more detail than your app or script. Use them to isolate issues.

Still stuck? Restart your server and try a simpler request to confirm connectivity.

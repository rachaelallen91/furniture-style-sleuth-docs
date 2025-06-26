
# Tutorial: Updating a Style Description

This tutorial shows how to update part of a style record using the `PATCH /styles` endpoint.

## Step 1: Pick a Style

Find the ID of the style you’d like to update. For example, use `1` for Midcentury Modern.

## Step 2: Send the PATCH Request

You only need to include the fields you want to update. For example:

```json
{
  "id": 1,
  "description": "Clean lines, warm woods, and functional design — a classic of the post-war era."
}
```

Send this to the `/styles` endpoint using `PATCH`.


## Step 3: Confirm the Update

A successful request returns:

- `200 OK` if the updated resource is returned
- `204 No Content` if the update succeeded but no response body is returned

To verify the changes, send a `GET` request to the specific style ID. For example:

```http
GET /styles/1
```

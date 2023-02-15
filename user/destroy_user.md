# Destroy an existing user

> Deletes an existing user for a company

## URL

`DELETE` /users/`:id`.json

## Query Parameters

- `id`: User ID

## Response: Success

Status Code: `200 OK`

```json
{
  "success": "The user was destroyed."
}
```

## Response: Failure

> Could happen is authorization fails `403` or record is not found `404`

Status Code: `403 Forbidden`

```
No Content
```

Status Code: `404 Not Found`

```
No Content
```

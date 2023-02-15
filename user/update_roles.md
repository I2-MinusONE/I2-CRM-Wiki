# Update Roles Assigned to a User

> This API updates the list of roles assigned to an existing user.

## URL

`PATCH /users/:id/roles.json`

## Query Parameters

- `id` - ID of the User whose roles are to be updates. 

## Request Body

```json
{
  "role_ids": [
    1,
    2,
    3,
    4 // other roles to be assigned to the user
  ]
}
```

## Response: Success

Status Code: `200 OK`

```json
{
  "success": "The roles were updated."
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

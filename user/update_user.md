# Update User

> This API updates an existing user.

Updates an existing user with the new data provided.

## Request

`PATCH /users/:id.json`

## Query Parameters

- `id`: ID of the User to patch

## Request Body

- `contact_id`: ID of the contact that the user is linked to.

## Response: Success

Status Code: `200 OK`

```json
{
  "id": 1,
  "contact": {
    "first_name": "Ikjot",
    "middle_name": "Singh",
    "last_name": "Dhody" //and so on
  }
}
```

## Response: Failure

Status Code: `400 Bad Request`

```json
{
  "error": "Invalid Parameters"
}
```

## Response: Failure

Status Code: `401 Unauthorized`

```json
{
  "error": "You are not authorized to access this resource. Please sign up or log in."
}
```

## Response: Failure

Status Code: `403 Forbidden`

```json
{
  "error": "Unauthorized"
}
```

## Response: Failure

Status Code: `422 Unprocessable Entity`

```json
{
  "error": "Unprocessable Entity"
}
```

## Response: Failure

Status Code: `500 Internal Server Error`

```json
{
  "error": "Internal Server Error"
}
```

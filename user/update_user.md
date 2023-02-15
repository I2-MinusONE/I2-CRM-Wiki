# Update User

> This API updates an existing user.

Updates an existing user with the new data provided.

## HTTP Request

`PUT /users/:id.json`

## Query Parameters

* `id`: ID of the User to patch

## Request Body

* `contact_id`: ID of the contact that the user is linked to.

## Response

The response will be a JSON object containing the updated user data.

## Examples

### Request

 ### PUT /users/1

```json
{
    "contact_id": 1234
}
```

### Response
```json
{
    "id": 1,
    "contact_id": 1234
}
```
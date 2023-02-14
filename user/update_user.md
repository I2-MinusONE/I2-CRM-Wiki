# Update User

> This API updates an existing user.

Updates an existing user with the new data provided.

## HTTP Request

`PUT /users/:id`

## Query Parameters

Parameter | Type | Description
--------- | ---- | -----------
id | integer | Required. The ID of the user to be updated.

## Request Body

The request body should be a JSON object containing the following fields:

Field | Type | Description
----- | ---- | -----------
contact_id | integer | Optional. ID of the contact that the user is linked to.

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
# Create a new user

> This WIKI page is maintained manually. Please contact the project manager for any clarifications.

This API creates a new user.

## URL
`POST` /users.json

The request should be a JSON object with the following properties:

* `contact_id`: `INTEGER` (required)
  ID of the contact that the user is linked to

Example request body:
```json
{
"contact_id": 123
}
```
## Response

If the user is successfully created, the response will be a JSON object with the following properties:

* `id`: `INTEGER`
  The ID of the newly created user.
* `contact_id`: `INTEGER`
  The ID of the contact that the user is linked to.

Example response body:
```json
{
"id": 456,
"contact_id": 123
}
```

If there was an error creating the user, the response will be a JSON object with an `error` property that contains a description of the error.

## HTTP Status Codes

* `201 Created` if the user is successfully created.
* `400 Bad Request` if the request is invalid.
* `500 Internal Server Error` if there was an error creating the user.

---

# Example

## Request

POST /users.json

Request body:

```json
{
  "contact_id": 123
}
```

## Response

HTTP/1.1 201 Created

### Response body:
```json
{
  "id": 456,
  "contact_id": 123
}
```
or
```json
{
  "error": "Failed to create user"
}
```
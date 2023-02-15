# Destroy a project

> Deletes an existing project

## URL

`DELETE` /projects/`:id`.json

## Query Parameters

- `id`: Project ID

## Response: Success

Status Code: `204 No Content`

## Response: Failure

> Could happen if authorization fails `403` or record is not found `404`

Status Code: `403 Forbidden`

Status Code: `404 Not Found`

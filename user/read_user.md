# Fetch an existing User

Retrieve the details of an existing User.

## URL

`GET` /users/`:id`.json

## Path Parameters

- `id` : `INTEGER` (required)
  The ID of the user that needs to be retrieved.

## Success Response

**Code**: `200 OK`

**Content Example**

```json
{
  "id": 123,
  "contact_id": 456
}
```

## Error Response

**Code**: `401 Unauthorized`

**Content**

```json
{
  "message": "Authentication failed"
}
```

**Code**: `404 Not Found`

**Content**

```json
{
  "message": "User not found"
}
```

**Code**: `500 Internal Server Error`

**Content**

```json
{
  "message": "Internal Server Error"
}
```

## Sample Request

```http
GET /users/123.json HTTP/1.1
Authorization: Bearer <access_token>
Content-Type: application/json
```

## Sample Response

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "id": 123,
    "contact_id": 456
}
```

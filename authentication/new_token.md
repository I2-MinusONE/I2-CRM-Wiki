# New Token
> Creates a new token for the user

## URL
`POST` /users/token.json

## Body Parameters
```json
{
    "email": "some@email.com",
    "password": "Password", // filtered
}
```

## Response: Success
Status Code: `201 Created`
```json
{
    "token": "string token"
}
```

## Response: Failure
> Could happen is authentication fails `401` or record is not found `404`

Status Code: `401 Not Authorized`
```
No Content
```

Status Code: `404 Not Found`
```
No Content
```
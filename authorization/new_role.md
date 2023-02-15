# New Role
> Creates a new role of a company

## URL
`POST` /roles.json

## Body Parameters
```json
{
    "name": "Role Name"
}
```

## Response: Success
Status Code: `201 Created`
```json
{
    "id": 1,
    "name": "Role Name",
    "users": []
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
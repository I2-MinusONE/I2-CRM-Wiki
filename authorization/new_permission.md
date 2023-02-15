# New permission
> Creates a new permission for a role

## URL
`POST` /permissions.json

## Body Parameters
```json
{
    "role_ids": [
        1, 2, 3 // a list of role ids to which this permission is assigned
    ],
    "entity_id": 1,
    "create_permission": true,
    "read_permission": true,
    "update_permission": true,
    "delete_permission": true,
    "admin_permission": true,
    "files_permission": true
}
```

## Response: Success
Status Code: `201 Created`
```json
{
    "role_ids": [
        1, 2, 3
    ],
    "entity": {
        "id": 1,
        "name": "Entity name 1",
    },
    "create_permission": true,
    "read_permission": true,
    "update_permission": true,
    "delete_permission": true,
    "admin_permission": true,
    "files_permission": true
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
# Get all Permissions
> Returns the list of permissions assigned to the user via his/her roles.

## URL
`GET` /my_permissions.json

## Response: Success
Status Code: `200 OK`
```json
[
    {
        "role_id": 1,
        "role_name": "Role Name 1",
        "permissions": [
            {
                "permission_id": 1,
                "permission_name": "Entity 1",
                "create_permission": true,
                "read_permission": true,
                "update_permission": true,
                "delete_permission": true,
                "admin_permission": true,
                "files_permission": true
            },
            {
                "permission_id": 2,
                "permission_name": "Entity 2",
                "create_permission": true,
                "read_permission": true,
                "update_permission": true,
                "delete_permission": true,
                "admin_permission": true,
                "files_permission": true
            } // and so on...
        ]
    },
    {
        "role_id": 2,
        "role_name": "Role Name 2",
        "permissions": [
            {
                "permission_id": 3,
                "permission_name": "Entity 1",
                "create_permission": true,
                "read_permission": true,
                "update_permission": true,
                "delete_permission": true,
                "admin_permission": true,
                "files_permission": true
            } // and so on...
        ]
    } // and so on...
]
```
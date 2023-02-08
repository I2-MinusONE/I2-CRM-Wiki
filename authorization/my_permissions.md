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
        "permissions": [
            {
                "permission_id": 1,
                "permission_name": "Entity 1",
                "permissions": "CRUDA"
                // { create, read, update, destroy, admin } as a string
            },
            {
                "permission_id": 2,
                "permission_name": "Entity 2",
                "permissions": "RU"
                // { create, read, update, destroy, admin } as a string
            } // and so on...
        ]
    },
    {
        "role_id": 2,
        "permissions": [
            {
                "permission_id": 3,
                "permission_name": "Entity 1",
                "permissions": "CR"
                // { create, read, update, destroy, admin } as a string
            } // and so on...
        ]
    } // and so on...
]
```
# Fetch Role
> Gets an existing role of a company

## URL
`GET` /roles/`:id`.json

## Query Parameters
* `id`: Role ID  

## Response: Success
Status Code: `200 OK`
```json
{
    "id": 1,
    "name": "Role Name",
    "users": [
        {
            "id": 1,
            "first_name": "First Name 1",
            // ...other fields of the user
        },
        {
            "id": 2,
            "first_name": "First Name 2",
            // ...other fields of the user
        },
        // and so on
    ],
    "permissions": [
        {
            "permission_id": 1,
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
        },
        {
            "permission_id": 2,
            "entity": {
                "id": 2,
                "name": "Entity name 2",
            },
            "create_permission": true,
            "read_permission": true,
            "update_permission": true,
            "delete_permission": true,
            "admin_permission": true,
            "files_permission": true
        } // and so on...
    ]
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
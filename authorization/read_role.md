# Fetch ROle
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
    "user_ids": [
        1, 2, // other users that have been assigned this role
    ],
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
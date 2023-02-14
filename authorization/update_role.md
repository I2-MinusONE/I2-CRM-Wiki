# Update an existing role
> Updates an existing role for a company

## URL
`PATCH` /roles/`:id`.json

## Query Parameters
* `id`: Role ID  

## Body Parameters
```json
{
    "name": "Role Name",
    "user_ids": [
        1, 2, // other users that have been assigned this role
    ],
    "permissions": [
        1, 2 // other permissions that are enabled for this role
    ]
}
```
This list of `field_name`s will be a subset of the fields in the parent [entity](./index.md).

## Response: Success
Status Code: `200 OK`
```json
{
    "success": "The role was updated.",
    "role": {
        "id": "Modified Role ID",
        // other role fields with modified data, user_ids, permissioms...
    }
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
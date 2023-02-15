# Destroy an existing permission
> Deletes an existing permission for a role

## URL
`DELETE` /permissions/`:id`.json

## Query Parameters
* `id`: Permission ID  

## Response: Success
Status Code: `200 OK`
```json
{
    "success": "The permission was destroyed."
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
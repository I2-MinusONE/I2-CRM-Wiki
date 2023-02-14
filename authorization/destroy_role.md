# Destroy an existing role
> Deletes an existing role for a company

## URL
`DELETE` /roles/`:id`.json

## Query Parameters
* `id`: Role ID  

## Response: Success
Status Code: `200 OK`
```json
{
    "success": "The role was destroyed."
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
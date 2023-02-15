# Destroy an existing organization
> Deletes an existing organization for a company

## URL
`DELETE` /organizations/`:id`.json

## Query Parameters
* `id`: Organization ID  

## Response: Success
Status Code: `200 OK`
```json
{
    "success": "The organization was destroyed."
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
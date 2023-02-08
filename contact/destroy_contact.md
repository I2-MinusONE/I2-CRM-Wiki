# Destroy an existing contact
> Deletes an existing contact for a company

## URL
`DELETE` /contacts/`:id`.json

## Query Parameters
* `id`: Contact ID  

## Response: Success
Status Code: `200 OK`
```json
{
    "success": "The contact was destroyed."
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
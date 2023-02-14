# Destroy an existing opportunity
> Deletes an existing opportunity for a company

## URL
`DELETE` /opportunities/`:id`.json

## Query Parameters
* `id`: Opportunity ID  

## Response: Success
Status Code: `200 OK`
```json
{
    "success": "The opportunity was destroyed."
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
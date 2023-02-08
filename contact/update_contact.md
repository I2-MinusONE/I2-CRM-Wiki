# Update an existing contact
> Updates an existing contact for a company

## URL
`PATCH` /contacts/`:id`.json

## Query Parameters
* `id`: Contact ID  

## Body Parameters
```json
{
    "field_name1": "modified data 1",
    "field_name2": "modified data 2",
    // and so on...
}
```
This list of `field_name`s will be a subset of the fields in the parent [entity](./index.md).

## Response: Success
Status Code: `200 OK`
```json
{
    "success": "The contact was updated.",
    "contact": {
        "id": "Modified Contact ID",
        // other contact fields with modified data...
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
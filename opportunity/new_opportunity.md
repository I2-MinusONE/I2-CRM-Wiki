# New Opportunity
> Creates a new opportunity of a company

## URL
`POST` /opportunities.json

## Body Parameters
```json
{
    "company_id": 1,
    "organization_id": 1,
    "name": "DELL LAPTOP ORDER 2023-20-12",
    "value": 2300,
    "currency": "$",
    "forecast_close_date": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
    "actual_close_date": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
    "created_by": 1, // some valid user_id
    "created_at": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
    "updated_at": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
    "misc": {
        "key1": "value1",
        "key2": "value2"
        // and so on
    }
}
```

## Response: Success
Status Code: `201 Created`
```json
{
    "id": 1,
    "comapny_id": 1,
    "organization_id": 1,
    "organization_name": "DELL INC",
    "name": "DELL LAPTOP ORDER 2023-20-12",
    "value": 2300,
    "currency": "$",
    "forecast_close_date": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
    "actual_close_date": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
    "created_by": 1, // some valid user_id
    "created_at": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
    "updated_at": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
    "misc": {
        "key1": "value1",
        "key2": "value2"
        // and so on
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
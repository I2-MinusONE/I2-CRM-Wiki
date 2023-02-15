# Fetch Organizations index
> Gets the index page records for organizations of a company

## URL

`GET` /organizations.json?{search_params}

### Search Params
We have the following search params:
- user_responsible_id={id}

## Response: Success
Status Code: `200 OK`
```json
[
  {
    "id": 1,
    "name": "DELL",
    "phone": "1234567890",
    "shipping_address": {
        "address_line_1": "Line 1",
        "address_line_2": "Line 2",
        "address_line_3": "Line 3",
        "city": "City",
        "pincode": "123345",
        "city": "City Name",
        "state": "State",
        "country": "Country Name"
    },
    "user_responsible": {
      "id": 1,
      "name": "Ishaan Singh"
    },
    "created_at": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
    "updated_at": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
  },
  // and so on
]
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

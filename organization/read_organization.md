# Fetch Organization
> Gets a particular organization of a company

## URL

`GET` /organizations/`:id`.json

## Query Parameters

- `id`: Organization ID

## Response: Success

Status Code: `200 OK`

```json
{
    "id": 1,
    "company_id": 1,
    "name": "DELL",
    "phone": "1234567890",
    "website": "www.some-website.com",
    "linkedin": "/handle",
    "facebook": "/handle",
    "twitter": "/handle",
    "billing_address": {
        "address_line_1": "Line 1",
        "address_line_2": "Line 2",
        "address_line_3": "Line 3",
        "city": "City",
        "pincode": "123345",
        "city": "City Name",
        "state": "State",
        "country": "Country Name"
    },
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
    "dates_to_rem": {
        "date_of_birth": "01-01-2001",
        "anniversary": "12-12-2022"
    },
    "user_responsible": {
      "id": 1,
      "name": "Ishaan Singh"
    },
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

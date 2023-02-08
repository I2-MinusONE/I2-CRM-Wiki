# Fetch Contact and Address Schema
> Gets the schema for a contact of a company

## URL
`GET` /contacts/`:id`.json

## Query Parameters
* `id`: Contact ID  

## Response: Success
Status Code: `200 OK`
```json
{
    "id": 1,
    "comapny_id": 1,
    "organization_id": 1,
    "type": "Customer",
    "first_name": "First",
    "middle_name": "Middle",
    "last_name": "Last",
    "designation": "Mr.",
    "email": "fake@email.com",
    "phone1": "1234567890",
    "phone2": "5678901234",
    "phone3": "9012345678",
    "address1": {
        "id": 1,
        "address_line_1": "Line 1",
        "address_line_2": "Line 2",
        "address_line_3": "Line 3",
        "city": "City",
        "pincode": "123345",
        "city": "City Name",
        "state": "State",
        "country": "Country Name"
    },
    "address2": null,
    "linkedin": "/some-tag",
    "facebook": "/some-tag",
    "twitter": "/some-tag",
    "dates_to_rem": {
        "date_of_birth": "01-01-2001",
        "anniversary": "12-12-2022"
    },
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
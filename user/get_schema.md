# Fetch User Schema
> Gets the schema for a user of a company

## URL
`GET` /users/schema.json

## Response: Success
Status Code: `200 OK`
```json
{
    "field_name1": {
        "type": "string", // datatype of the field
        "options": {
            "id1": "description 1",
            "id2": "description 2" // and so on...
        }
    },
    "field_name2": {},
    // and so on...
    // one of these fields will be for the address schema as well
}
```

> This list of `field_name`s will be a subset of the fields in the parent [entity](./index.md).  

> The `type`s can be one of
> * `INTEGER` Number
> * `STRING` Textfield
> * `ENUM` Dropdown
> * `DATETIME` Calendar and time selector
> * `JSON OBJECT` An object with custom fields
> * `JSON ARRAY` Multiselect or a list of values
# Fetch Opportunities index

> Gets the index page records for opportunities of a company

## URL

`GET` /opportunities.json?{search_params}

### Search Params
We have the following search params:
- opportunity_value_greater_than={value}
- opportunity_value_lower_than={value}
- pipeline_status={status-completed/in_progress/failed}
- user_responsible_id={id}
- organization_id={id}


## Response: Success

Status Code: `200 OK`

```json
[
  {
    "id": 1,
    "company_id": 1,
    "organization_id": 1,
    "organization_name": "DELL INC",
    "name": "DELL LAPTOP ORDER 2023-20-12",
    "value": 2300,
    "currency": "$",
    "forecast_close_date": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
    "user_responsible_id": 1, // some valid user_id
    "user_responsible_name": "Ikjot Singh Dhody"
  },
  {
    "id": 2,
    "company_id": 1,
    "organization_id": 1,
    "organization_name": "DELL INC",
    "name": "DELL MOUSE ORDER 2023-20-12",
    "value": 1200,
    "currency": "$",
    "forecast_close_date": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
    "user_responsible_id": 1, // some valid user_id
    "user_responsible_name": "Ikjot Singh Dhody"
  }
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

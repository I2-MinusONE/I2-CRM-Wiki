# Fetch Opportunity

> Gets a particular opportunity of a company

## URL

`GET` /opportunities/`:id`.json

## Query Parameters

- `id`: Opportunity ID

## Response: Success

Status Code: `200 OK`

```json
{
  "id": 1,
  "company_id": 1,
  "organization_id": 1,
  "organization_name": "DELL INC",
  "name": "DELL LAPTOP ORDER 2023-20-12",
  "value": 2300,
  "currency": "$",
  "forecast_close_date": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
  "actual_close_date": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
  "user_responsible_id": 1, // some valid user_id
  "user_responsible_name": "Ikjot Singh Dhody",
  "created_at": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
  "updated_at": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
  "misc": {
    "key1": "value1",
    "key2": "value2"
    // and so on
  },
  "pipeline": {
    "1": {
      "name_of_stage": "Quotation sent",
      "activities": [
        {
          "type": "event",
          "title": "Meeting with Raj",
          "location_name": "Meeting Room 2",
          "location_id": 121,
          "start_time": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
          "end_time": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
          "organizer_name": "Ikjot Singh",
          "organizer_id": 112,
          "description": "",
          "visibility": "private"
        },
        {
          "type": "task",
          "title": "Finish Paperwork",
          "category": "email/phone/todo/follow_up/etc",
          -- Next few fields depend on category of task
          "start_date": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
          "due_date": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
          "reminder_date": "timestamp as yyyy-MM-dd'T'HH:mm:ssZZZZ",
          "user_name": "Ikjot Singh",
          "user_id": 112,
          "description": "",
          "visibility": "private",
          "priority": 67
          -- number out of 100
        }
      ],
      "status": "completed"
    },
    "2": {
      "name_of_stage": "Negotiations",
      "activities": [],
      "status": "in_progress"
    }
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

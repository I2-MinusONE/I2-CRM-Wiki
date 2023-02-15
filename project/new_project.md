# New Project

Creates a new project record.

## URL

`POST` /projects.json

## Parameters

- `team_id` (required):

  ID of the team to which this record belongs to.

- `opportunity_id` (required):

  ID of the opportunity that was converted.

- `value` (required):
  Value of the converted opportunity.
- `currency` (required):
  Currency in which the opportunity was converted.
- `converted_at` (required):
  Date and time at which the opportunity was converted.
- `created_by` (required):
  User responsible for converting the opportunity.
- `misc` (optional):
  Stores miscellaneous information about the converted opportunity.
- `pipeline_id` (required):
  The pipeline ID of the converted opportunity.

## Response: Success

Status Code: `201 Created`

```json
{
  "id": 12345,
  "team_id": 67890,
  "opportunity_id": 13579,
  "value": 1000,
  "currency": "$",
  "converted_at": "2022-03-01 15:00:00",
  "created_by": 54321,
  "misc": {},
  "pipeline_id": 98765,
  "created_at": "2022-03-01 15:00:00",
  "updated_at": "2022-03-01 15:00:00"
}
```

## Response: Failure

Status Code: `400 Bad Request`

```json
{
  "error": "Invalid Parameters"
}
```

## Response: Failure

Status Code: `401 Unauthorized`

```json
{
  "error": "You are not authorized to access this resource. Please sign up or log in."
}
```

## Response: Failure

Status Code: `403 Forbidden`

```json
{
  "error": "Unauthorized"
}
```

## Response: Failure

Status Code: `422 Unprocessable Entity`

```json
{
  "error": "Unprocessable Entity"
}
```

## Response: Failure

Status Code: `500 Internal Server Error`

```json
{
  "error": "Internal Server Error"
}
```

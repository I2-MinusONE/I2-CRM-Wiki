# Get a single project

> Returns a single project belonging to a team.

## URL

`GET` /projects/`:id`.json

## Parameters

- `id`: Project ID

## Response: Success

Status Code: `200 OK`

```json
{
  "id": 1,
  "team_id": 1,
  "project_id": 1,
  "opportunity_id": 1,
  "value": 1000,
  "currency": "$",
  "converted_at": "2023-02-14 12:00:00",
  "created_by": 1,
  "updated_at": "2023-02-14 12:00:00",
  "misc": {},
  "pipeline_id": 1
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

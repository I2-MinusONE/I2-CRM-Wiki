# Get a list of projects
> Returns a list of projects belonging to a team.

## URL
`GET` /projects.json

## Parameters
* `team_id`: Team ID

## Response: Success
Status Code: `200 OK`
```json
{
    "projects": [
        {
            "id": 1,
            "team_id": 1,
            "project_id": 1,
            "opportunity_converted_id": 1,
            "value": 1000,
            "currency": "USD",
            "converted_at": "2023-02-14 12:00:00",
            "converted_by": 1,
            "updated_at": "2023-02-14 12:00:00",
            "misc": {},
            "pipeline_id": 1
        },
        {
            "id": 2,
            "team_id": 1,
            "project_id": 2,
            "opportunity_converted_id": 2,
            "value": 2000,
            "currency": "USD",
            "converted_at": "2023-02-14 12:00:00",
            "converted_by": 1,
            "updated_at": "2023-02-14 12:00:00",
            "misc": {},
            "pipeline_id": 2
        }
    ]
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

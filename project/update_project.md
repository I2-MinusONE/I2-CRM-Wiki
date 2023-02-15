# Update a project
> Updates an existing project for a team

## URL
`PUT` /projects/`:project_id`.json

## Path Parameters
* `team_id` : ID of the team that the project belongs to
* `project_id` : ID of the project that is being updated

## Request Parameters
The following fields can be updated:
* `opportunity_converted_id` : ID of the opportunity that was converted
* `value` : Value of the converted opportunity
* `currency` : Currency in which the opportunity was converted
* `converted_at` : Date and time at which the opportunity was converted
* `converted_by` : User responsible for converting the opportunity
* `misc` : Miscellaneous information about the converted opportunity
* `pipeline_id` : The pipeline ID of the converted opportunity

The request body should be a JSON object containing one or more of these fields.

## Response: Success
Status Code: `200 OK`
```json
{
    "project": {
        "id": 1,
        "team_id": 1,
        "project_id": 1234,
        "opportunity_converted_id": 5678,
        "value": 10000,
        "currency": "USD",
        "converted_at": "2023-02-14 12:00:00",
        "converted_by": 123,
        "misc": {
            "notes": "Converted opportunity from Q1 sales push"
        },
        "pipeline_id": 9876,
        "updated_at": "2023-02-14 14:30:00"
    }
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
    "error": "Unauthorized"
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

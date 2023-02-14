# Project

> This WIKI page is maintained manually. Please use the project manager for any clarifications.

This module manages projects via API. Projects are the current/former projects of
the company that is using our CRM software. They use and manage their CRM Project.

---

# Use Cases

- [Fetch Project Schema](./get_schema.md)
- [Create a new project](./new_project.md)
- [Read an existing project](./read_project.md)
- [Update an existing project](./update_project.md)
- [Destroy an existing project](./destroy_project.md)

---

# Entity Description

## Project

The following is the exhaustive list of all characteristics of this enitity.

* `id`: `INTEGER`
  A unique ID self-assigned to this record.
* `team_id`: `INTEGER`
  ID of the team to which this record belongs to.
* `project_id`: `INTEGER`
  ID of the project to which this record belongs to.
* `opportunity_converted_id`: `INTEGER`
  ID of the opportunity that was converted.
* `value`: `INTEGER`
  Value of the converted opportunity.
* `currency`: `STRING`
  Currency in which the opportunity was converted.
* `converted_at`: `DATETIME`
  Date and time at which the opportunity was converted.
* `converted_by`: `INTEGER`
  User responsible for converting the opportunity.
* `updated_at`: `DATETIME`
  Date and time at which the record was last updated.
* `misc`: `JSON OBJECT`
  Stores miscellaneous information about the converted opportunity.
* `pipeline_id`: `INTEGER`
  The pipeline ID of the converted opportunity.

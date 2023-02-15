# User

> This WIKI page is maintained manually. Please contact the project manager for any clarifications.

This module manages users via API. Users are the current/former employees of
the company that is using our CRM software. They use and manage their CRM Project.

---

# Use Cases

- [Fetch User Schema](./get_schema.md)
- [Create a new user](./new_user.md)
- [Read an existing user](./read_user.md)
- [Update an existing user](./update_user.md)
- [Destroy an existing user](./destroy_user.md)
- [Fetch all roles of a user](./get_roles.md)
- [Update list of roles assigned to a user](./update_roles.md)

---

# Entity Description

## User

The following is the exhaustive list of all characteristics of this enitity.

* `id`: `INTEGER`
  A unique ID self-assigned to this record.
* `contact_id`: `INTEGER`
  ID of the contact that the user is linked to
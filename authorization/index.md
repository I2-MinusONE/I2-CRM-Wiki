# Authorization
> This WIKI page is maintained manually. Please contact the project manager for any clarifications.

This module manages user authorization. We do not use a token-claim based approach, but have a static role-permission-access-control (RBAC) model.

---

## General Instruction

The `BEARER` Authorization header will contain the user-token in every request. Authorization will be done on a per-request basis.

## Use Cases

* [Get all permissions for a user](./my_permissions.md)  
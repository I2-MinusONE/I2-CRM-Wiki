# Authorization
> This WIKI page is maintained manually. Please contact the project manager for any clarifications.

This module manages user authorization. We do not use a token-claim based approach, but have a static role-permission-access-control (RBAC) model.

---

## General Instruction

The `BEARER` Authorization header will contain the user-token in every request. Authorization will be done on a per-request basis.

## Use Cases

* [Get all permissions for a user](./my_permissions.md)  
* [Get all Roles](./get_all_roles.md)  
* [Create a new role](./new_role.md)  
* [Read an existing role](./read_role.md)  
* [Update an existing role](./update_role.md)  
* [Delete an exiting role](./destroy_role.md)  
* [Create a new permission](./new_permission.md)  
* [Delete an exiting permission](./destroy_permission.md)  

---

# Entitiy Description

## Role
The following is the exhaustive list of all characteristics of this enitity.
* `id: INTEGER`  
A unique ID self-assigned to this record.
* `comapny_id: INTEGER`  
ID of the Company to which this record belongs to.
* `name: STRING`

## Related Entity - Permission
The following is the exhaustive list of all characteristics of this enitity.
* `id: INTEGER`  
A unique ID self-assigned to this record.
* `role_id: INTEGER`  
* `access: STRING`  
Stores access set { create, read, update, destroy, admin } as a string - CRUDA

## Related Entity - Assignment
The following is the exhaustive list of all characteristics of this enitity.
* `id: INTEGER`  
A unique ID self-assigned to this record.
* `role_id: INTEGER`  
* `user_id: INTEGER`  

---

# Relationship Description

A role defines a blueprint profile for a user. Every role has associated permissions. A permission defines the granularity of access to a schema entity in the database. An assignment records how a role and user are related.

With such a RBAC, a user can be assigned several roles, and several users can have the same role. The permissions associated with a role define what accesses those permisions allow the user to have.
# Opportunity
> This WIKI page is maintained manually. Please opportunity the project manager for any clarifications.

This module manages organizations of a company via API. Organizations are companies that out customer-companied deal with. Every contact, opportunity, job, etc belongs to an organization.

---

# Use Cases

* [Fetch Organization Schema](./get_schema.md)
* [Fetch All Organizations](./get_all_organizations.md)
* [Create a new Organization](./new_organization.md)  
* [Read an existing Organization](./read_organization.md)  
* [Update an existing Organization](./update_organization.md)  
* [Destroy an existing Organization](./destroy_organization.md) 

---

# Entity Description

## Organization
The following is the exhaustive list of all characteristics of this enitity.
* `id: INTEGER`  
A unique ID self-assigned to this record.
* `company_id: INTEGER`  
ID of the Company to which this record belongs to.
* `name: STRING`
* `phone: STRING`
* `website: STRING`
* `linkedin: STRING`
* `facebook: STRING`
* `twitter: STRING`
* `billing_address: JSON OBJECT`
* `shipping_address: JSON OBJECT`
* `dates_to_rem: JSON OBJECT`
* `contact_responsible: JSON OBJECT`
Point of contact for this organization
* `created_at: DATETIME`
* `updated_at: DATETIME`
* `misc: JSON OBJECT`
Stores miscellaneous information about the opportunity.
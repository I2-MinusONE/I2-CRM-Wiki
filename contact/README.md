# Contact
> This WIKI page is maintained manually. Please contact the project manager for any clarifications.

This module manages contacts via API. Contacts are the basic units of the app. Several other entities like users, jobs, opportunities, etc. use Contacts.

---

# Use Cases

* [Fetch Contact Schema](./get_schema.md)
* [Create a new contact](./new_contact.md)  
* [Read an existing contact](./read_contact.md)  
* [Update an existing contact](./update_contact.md)  
* [Destroy an existing contact](./destroy_contact.md) 

---

# Entitiy Description

## Contact
The following is the exhaustive list of all characteristics of this enitity.
* `id: INTEGER`  
A unique ID self-assigned to this record.
* `comapny_id: INTEGER`  
ID of the Company to which this record belongs to.
* `organization_id: INTEGER`  
ID of the Organization this contact belongs to.
* `type: ONE OF { Customer, Lead, Supplier, etc }`  
Contacts can be of various types, that can be set by the company admin.
* `first_name: STRING`
* `middle_name: STRING`
* `last_name: STRING`
* `designation: STRING`  
Any title that this contact is recognized by.
* `email: STRING`
* `phone1: STRING`
* `phone2: STRING`
* `phone3: STRING`
* `address1: JSON OBJECT`  
This is an object of the Address Entitiy.
* `address2: JSON OBJECT`  
This is an object of the Address Entitiy.
* `linkedin: STRING`
* `facebook: STRING`
* `twitter: STRING`
* `dates_to_rem: JSON OBJECT`  
This is a JSON array with many key-value pairs.
* `created_by: INTEGER REFERENCING USER`
* `created_at: DATETIME`
* `updated_at: DATETIME`
* `misc: JSON OBJECT`  
Stores miscellaneous information about the contact.

## Related Entity - Address
The following is the exhaustive list of all characteristics of this enitity.
* `id: INTEGER`  
A unique ID self-assigned to this record.
* `address_line_1: STRING`
* `address_line_2: STRING`
* `address_line_3: STRING`
* `city: STRING`
* `pincode: STRING`
* `city: STRING`
* `state: STRING`
* `country: STRING`
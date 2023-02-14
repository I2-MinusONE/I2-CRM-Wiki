# Opportunity
> This WIKI page is maintained manually. Please opportunity the project manager for any clarifications.

This module manages opportunities via API. Opportunities are the potential projects for a company. Each project has a prequel opportunity - that gets converted into that project.

---

# Use Cases

* [Fetch Opportunity Schema](./get_schema.md)
* [Fetch All Opportunities](./get_all_opportunities.md)
* [Create a new opportunity](./new_opportunity.md)  
* [Read an existing opportunity](./read_opportunity.md)  
* [Update an existing opportunity](./update_opportunity.md)  
* [Destroy an existing opportunity](./destroy_opportunity.md) 

---

# Entity Description

## Opportunity
The following is the exhaustive list of all characteristics of this enitity.
* `id: INTEGER`  
A unique ID self-assigned to this record.
* `company_id: INTEGER`  
ID of the Company to which this record belongs to.
* `organization_id: INTEGER`  
ID of the Organization this opportunity belongs to.
* `name: STRING`  
* `pipeline_id: INTEGER`
The pipeline ID of the opportunity.
* `value: INTEGER`
* `currency: STRING`
* `forecast_close_date: DATETIME`  
* `actual_close_date: DATETIME`
* `created_by: INTEGER`
User responsible for creating opportunity
* `created_at: DATETIME`
* `updated_at: DATETIME`
* `misc: JSON OBJECT`  
Stores miscellaneous information about the opportunity.
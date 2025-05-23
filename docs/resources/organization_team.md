---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tailor_organization_team Resource - terraform-provider-tailor"
subcategory: ""
description: |-
  The organization team resource represents an organization team in Tailor.
---

# tailor_organization_team (Resource)

The organization team resource represents an organization team in Tailor.

## Example Usage

```terraform
resource "tailor_organization_team" "the_501st_legion" {
  organization_id = data.tailor_organization.galactic_empire.id
  name            = "501st legion"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) The name of this organization team.
- `organization_id` (String) The ID of the organization that the organization team belongs to.

### Read-Only

- `id` (String) The computed ID of the organization team.

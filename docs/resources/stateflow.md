---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tailor_stateflow Resource - terraform-provider-tailor"
subcategory: ""
description: |-
  The stateflow resource represents a StateFlow in Tailor.
---

# tailor_stateflow (Resource)

The stateflow resource represents a StateFlow in Tailor.



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `namespace` (String) Namespace name for this StateFlow.
- `workspace_id` (String) The ID of the workspace that the StateFlow belongs to.

### Optional

- `admins` (List of String) The list of admins for this StateFlow.
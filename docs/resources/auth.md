---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tailor_auth Resource - terraform-provider-tailor"
subcategory: ""
description: |-
  The auth resource represents an auth namespace in Tailor.
---

# tailor_auth (Resource)

The auth resource represents an auth namespace in Tailor.

## Example Usage

```terraform
resource "tailor_auth" "starwars_auth" {
  workspace_id = tailor_workspace.starwars.id
  namespace    = "starwars-auth"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `namespace` (String) Namespace name for this auth resource.
- `workspace_id` (String) The ID of the workspace that the auth namespace belongs to.
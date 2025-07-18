---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tailor_auth_user_profile_config Resource - terraform-provider-tailor"
subcategory: ""
description: |-
  The auth_user_profile_config resource represents a user profile configuration in Tailor.
---

# tailor_auth_user_profile_config (Resource)

The auth_user_profile_config resource represents a user profile configuration in Tailor.

## Example Usage

```terraform
resource "tailor_auth_user_profile_config" "character" {
  workspace_id = tailor_workspace.starwars.id
  namespace    = tailor_auth.starwars_auth.namespace

  tailordb_config = {
    namespace      = tailor_tailordb.galaxy.namespace
    type           = tailor_tailordb_type.character.name
    username_field = "email"
    attribute_fields = [
      "roles"
    ]
  }
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `namespace` (String) The auth namespace of the user profile configuration.
- `tailordb_config` (Attributes) The configuration for the TailorDB type. (see [below for nested schema](#nestedatt--tailordb_config))
- `workspace_id` (String) The ID of the workspace that the user profile configuration belongs to.

### Read-Only

- `id` (String) The unique identifier of the resource.

<a id="nestedatt--tailordb_config"></a>
### Nested Schema for `tailordb_config`

Required:

- `namespace` (String) The namespace of the TailorDB.
- `type` (String) The type of the TailorDB.
- `username_field` (String) The field that contains the username.

Optional:

- `attribute_fields` (List of String) The list of attribute fields.
- `attribute_map` (Map of String) The map of attributes.
- `tenant_id_field` (String) The field that contains the tenant ID.

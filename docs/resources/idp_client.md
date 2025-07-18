---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tailor_idp_client Resource - terraform-provider-tailor"
subcategory: ""
description: |-
  The idp_client resource represents an Identity Provider (IdP) client in Tailor.
---

# tailor_idp_client (Resource)

The idp_client resource represents an Identity Provider (IdP) client in Tailor.

## Example Usage

```terraform
resource "tailor_idp_client" "default_client" {
  workspace_id = tailor_workspace.starwars.id
  namespace    = tailor_idp.starwars_idp.namespace

  name         = "default-client"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) The name of this IdP client.
- `namespace` (String) The namespace name of the IdP service for this IdP client.
- `workspace_id` (String) The ID of the workspace that the IdP client belongs to.

### Read-Only

- `client_id` (String) The computed client ID.
- `client_secret` (String, Sensitive) The computed client secret.
- `id` (String) The unique identifier of the resource.

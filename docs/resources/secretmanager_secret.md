---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tailor_secretmanager_secret Resource - terraform-provider-tailor"
subcategory: ""
description: |-
  The secretmanager_secret resource represents a Secret in Tailor.
---

# tailor_secretmanager_secret (Resource)

The secretmanager_secret resource represents a Secret in Tailor.

## Example Usage

```terraform
resource "tailor_secretmanager_secret" "death_star_plan" {
  workspace_id = tailor_workspace.starwars.id
  vault_name   = tailor_secretmanager_vault.default.name

  name  = "death-star-plan"
  value = "The details of the Death Star plan are a secret."
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) The name of this Secret.
- `vault_name` (String) The vault name for this Secret belongs to.
- `workspace_id` (String) The ID of the workspace that the Secret belongs to.

### Optional

> **NOTE**: [Write-only arguments](https://developer.hashicorp.com/terraform/language/resources/ephemeral#write-only-arguments) are supported in Terraform 1.11 and later.

- `value` (String, Sensitive, Deprecated) The value of this Secret. (Deprecated) Use `vault_wo` instead.
- `value_wo` (String, [Write-only](https://developer.hashicorp.com/terraform/language/resources/ephemeral#write-only-arguments)) The value of this Secret.
- `value_wo_version` (Number) The version of the value of this Secret. Change this to update the value of the Secret.

### Read-Only

- `id` (String) The unique identifier of the resource.

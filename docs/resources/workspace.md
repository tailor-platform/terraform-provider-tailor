---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tailor_workspace Resource - terraform-provider-tailor"
subcategory: ""
description: |-
  The workspace resource represents a Workspace in Tailor.
---

# tailor_workspace (Resource)

The workspace resource represents a Workspace in Tailor.



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) The name of the workspace.
- `region` (String) The region of the workspace.

### Optional

- `delete_protection` (Boolean) Whether the workspace is protected from deletion.
- `folder_id` (String) The ID of the organization folder that the workspace belongs to.
- `organization_id` (String) The ID of the organization that the workspace belongs to.

### Read-Only

- `id` (String) The ID of the workspace.

---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tailor_pipeline Resource - terraform-provider-tailor"
subcategory: ""
description: |-
  The pipeline resource represents a pipeline in Tailor.
---

# tailor_pipeline (Resource)

The pipeline resource represents a pipeline in Tailor.



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `namespace` (String) Namespace name for this pipeline.
- `workspace_id` (String) The ID of the workspace that the pipeline belongs to.

### Optional

- `common_sdl` (String) The common SDL for this pipeline.
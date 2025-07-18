---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "tailor_application Resource - terraform-provider-tailor"
subcategory: ""
description: |-
  The application resource represents an application in Tailor. An application contains a set of subgraphs that are used to define the application's behavior. The application resource may also contains configuration for user authentication and CORS.
---

# tailor_application (Resource)

The application resource represents an application in Tailor. An application contains a set of subgraphs that are used to define the application's behavior. The application resource may also contains configuration for user authentication and CORS.

## Example Usage

```terraform
resource "tailor_application" "starwars" {
  workspace_id = tailor_workspace.starwars.id

  name = "star-wars"
  cors = [
    "http://localhost:3000", # Allow local development
  ]
  allowed_ip_addresses = [
    "0.0.0.0/0", # Allow all
  ]
  auth = {
    namespace       = tailor_auth.starwars_auth.namespace
    idp_config_name = tailor_auth_idp_config.oidc.name
  }
  subgraphs = [
    {
      type      = "tailordb"
      namespace = tailor_tailordb.galaxy.namespace
    },
    {
      type      = "stateflow"
      namespace = tailor_stateflow.construction.namespace
    },
    {
      type      = "pipeline"
      namespace = tailor_pipeline.starwars.namespace
    },
    {
      type      = "auth"
      namespace = tailor_auth.starwars_auth.namespace
    }
  ]
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) The name of the application.
- `subgraphs` (Attributes List) The list of subgraphs to use for the application. (see [below for nested schema](#nestedatt--subgraphs))
- `workspace_id` (String) The ID of the workspace that the application belongs to.

### Optional

- `allowed_ip_addresses` (List of String) The list of allowed IP addresses in CIDR notation.
- `auth` (Attributes) The auth configuration of the application for user authentication. (see [below for nested schema](#nestedatt--auth))
- `cors` (List of String) The list of allowed origins for CORS.
- `disable_introspection` (Boolean) Disable GraphQL introspection for the application.
- `disabled` (Boolean) Whether the application is disabled.

### Read-Only

- `domain` (String) The computed domain of the application.
- `id` (String) The unique identifier of the resource.
- `url` (String) The computed URL of the application.

<a id="nestedatt--subgraphs"></a>
### Nested Schema for `subgraphs`

Required:

- `namespace` (String) The namespace of the subgraph.
- `type` (String) The type of the subgraph. Can be one of 'tailordb', 'pipeline', 'stateflow', 'auth', 'idp'.


<a id="nestedatt--auth"></a>
### Nested Schema for `auth`

Required:

- `namespace` (String) The namespace of the auth resource.

Optional:

- `idp_config_name` (String) The name of the auth_idp_config resource.

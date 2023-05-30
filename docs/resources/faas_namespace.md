---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "gcore_faas_namespace Resource - terraform-provider-gcore"
subcategory: ""
description: |-
  Represent FaaS namespace
---

# gcore_faas_namespace (Resource)

Represent FaaS namespace

## Example Usage

```terraform
provider gcore {
  permanent_api_token = "251$d3361.............1b35f26d8"
}

resource "gcore_faas_namespace" "ns" {
        project_id = 1
        region_id = 1
        name = "testns"
        description = "test description"
        envs = {
            BIG_ENV = "EXAMPLE"
        }
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **name** (String)

### Optional

- **description** (String)
- **envs** (Map of String)
- **id** (String) The ID of this resource.
- **project_id** (Number)
- **project_name** (String)
- **region_id** (Number)
- **region_name** (String)

### Read-Only

- **created_at** (String)
- **status** (String)

## Import

Import is supported using the following syntax:

```shell
# import using <project_id>:<region_id>:<namespace_name> format
terraform import gcore_faas_namespace.test 1:6:ns
```
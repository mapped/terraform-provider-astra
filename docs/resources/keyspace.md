---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "astra_keyspace Resource - terraform-provider-astra"
subcategory: ""
description: |-
  astra_keyspace provides a keyspace resource. Keyspaces are groupings of tables for Cassandra. astra_keyspace resources are associated with a database id. You can have multiple keyspaces per DB in addition to the default keyspace provided in the astra_database resource.
---

# astra_keyspace (Resource)

`astra_keyspace` provides a keyspace resource. Keyspaces are groupings of tables for Cassandra. `astra_keyspace` resources are associated with a database id. You can have multiple keyspaces per DB in addition to the default keyspace provided in the `astra_database` resource.

## Example Usage

```terraform
resource "astra_keyspace" "example" {
  name        = "example"
  database_id = "48bfc13b-c1a5-48db-b70f-b6ef9709872b"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `database_id` (String) Astra database to create the keyspace.
- `name` (String) Keyspace name can have up to 48 alpha-numeric characters and contain underscores; only letters and numbers are supported as the first character.

### Optional

- `id` (String) The ID of this resource.

## Import

Import is supported using the following syntax:

```shell
# the import id includes the database_id and the keyspace name.
terraform import astra_keyspace.example 48bfc13b-c1a5-48db-b70f-b6ef9709872b/keyspace/example
```

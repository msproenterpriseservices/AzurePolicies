# Private endpoint should be enabled for MariaDB servers

## Display Name

Private endpoint should be enabled for MariaDB servers

## Mode

`Indexed`

## Description

Private endpoint connections enforce secure communication by enabling private connectivity to Azure Database for MariaDB. Configure a private endpoint connection to enable access to traffic coming only from known networks and prevent access from all other IP addresses, including within Azure.

## Built-In Reference

Modified from: [MariaDB_EnablePrivateEndPoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/MariaDB_EnablePrivateEndPoint_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "private_endpoint_should_be_enabled_for_mariadb_servers" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "private_endpoint_should_be_enabled_for_mariadb_servers"
  display_name          = "Private endpoint should be enabled for MariaDB servers"
  policy_description    = "Private endpoint connections enforce secure communication by enabling private connectivity to Azure Database for MariaDB. Configure a private endpoint connection to enable access to traffic coming only from known networks and prevent access from all other IP addresses, including within Azure."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

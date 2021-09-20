# Public network access should be disabled for PostgreSQL servers

## Display Name

Public network access should be disabled for PostgreSQL servers

## Mode

`All`

## Description

Disable the public network access property to improve security and ensure your Azure Database for PostgreSQL can only be accessed from a private endpoint. This configuration disables access from any public address space outside of Azure IP range, and denies all logins that match IP or virtual network-based firewall rules.

## Built-In Reference

Modified from: [PostgreSQL_DisablePublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/PostgreSQL_DisablePublicNetworkAccess_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "public_network_access_should_be_disabled_for_postgresql_servers" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "public_network_access_should_be_disabled_for_postgresql_servers"
  display_name          = "Public network access should be disabled for PostgreSQL servers"
  policy_description    = "Disable the public network access property to improve security and ensure your Azure Database for PostgreSQL can only be accessed from a private endpoint. This configuration disables access from any public address space outside of Azure IP range, and denies all logins that match IP or virtual network-based firewall rules."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

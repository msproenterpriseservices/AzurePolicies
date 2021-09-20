# Public network access should be disabled for MySQL flexible servers

## Display Name

Public network access should be disabled for MySQL flexible servers

## Mode

`All`

## Description

Disabling the public network access property improves security by ensuring your Azure Database for MySQL flexible servers can only be accessed from a private endpoint. This configuration strictly disables access from any public address space outside of Azure IP range and denies all logins that match IP or virtual network-based firewall rules.

## Built-In Reference

Modified from: [MySQL_FlexibleServers_DisablePublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/MySQL_FlexibleServers_DisablePublicNetworkAccess_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "public_network_access_should_be_disabled_for_mysql_flexible_servers" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "public_network_access_should_be_disabled_for_mysql_flexible_servers"
  display_name          = "Public network access should be disabled for MySQL flexible servers"
  policy_description    = "Disabling the public network access property improves security by ensuring your Azure Database for MySQL flexible servers can only be accessed from a private endpoint. This configuration strictly disables access from any public address space outside of Azure IP range and denies all logins that match IP or virtual network-based firewall rules."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

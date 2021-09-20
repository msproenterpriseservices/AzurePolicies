# Public network access on Azure SQL Database should be disabled

## Display Name

Public network access on Azure SQL Database should be disabled

## Mode

`All`

## Description

Disabling the public network access property improves security by ensuring your Azure SQL Database can only be accessed from a private endpoint. This configuration denies all logins that match IP or virtual network based firewall rules.

## Built-In Reference

Modified from: [SqlServer_PublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/SqlServer_PublicNetworkAccess_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "public_network_access_on_azure_sql_database_should_be_disabled" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "public_network_access_on_azure_sql_database_should_be_disabled"
  display_name          = "Public network access on Azure SQL Database should be disabled"
  policy_description    = "Disabling the public network access property improves security by ensuring your Azure SQL Database can only be accessed from a private endpoint. This configuration denies all logins that match IP or virtual network based firewall rules."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

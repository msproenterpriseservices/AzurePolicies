# Private endpoint connections on Azure SQL Database should be enabled

## Display Name

Private endpoint connections on Azure SQL Database should be enabled

## Mode

`Indexed`

## Description

Private endpoint connections enforce secure communication by enabling private connectivity to Azure SQL Database.

## Built-In Reference

Modified from: [SqlServer_PrivateEndpoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SQL/SqlServer_PrivateEndpoint_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "private_endpoint_connections_on_azure_sql_database_should_be_enabled" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "private_endpoint_connections_on_azure_sql_database_should_be_enabled"
  display_name          = "Private endpoint connections on Azure SQL Database should be enabled"
  policy_description    = "Private endpoint connections enforce secure communication by enabling private connectivity to Azure SQL Database."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

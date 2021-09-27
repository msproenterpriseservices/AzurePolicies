# Public network access on Azure Data Factory should be disabled

## Display Name

Public network access on Azure Data Factory should be disabled

## Mode

`All`

## Description

Disabling the public network access property improves security by ensuring your Azure Data Factory can only be accessed from a private endpoint.

## Built-In Reference

Modified from: [DataFactory_PublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Data%20Factory/DataFactory_PublicNetworkAccess_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "public_network_access_on_azure_data_factory_should_be_disabled" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "public_network_access_on_azure_data_factory_should_be_disabled"
  display_name          = "Public network access on Azure Data Factory should be disabled"
  policy_description    = "Disabling the public network access property improves security by ensuring your Azure Data Factory can only be accessed from a private endpoint."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

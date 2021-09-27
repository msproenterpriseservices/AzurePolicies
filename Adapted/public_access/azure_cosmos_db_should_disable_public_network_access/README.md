# Azure Cosmos DB should disable public network access

## Display Name

Azure Cosmos DB should disable public network access

## Mode

`All`

## Description

Disabling public network access improves security by ensuring that your CosmosDB account isn't exposed on the public internet. Creating private endpoints can limit exposure of your CosmosDB account.

## Built-In Reference

Modified from: [Cosmos_PrivateNetworkAccess_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Cosmos%20DB/Cosmos_PrivateNetworkAccess_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_cosmos_db_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_cosmos_db_should_disable_public_network_access"
  display_name          = "Azure Cosmos DB should disable public network access"
  policy_description    = "Disabling public network access improves security by ensuring that your CosmosDB account isn't exposed on the public internet. Creating private endpoints can limit exposure of your CosmosDB account."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

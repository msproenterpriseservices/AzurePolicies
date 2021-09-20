# Azure Cognitive Search services should disable public network access

## Display Name

Azure Cognitive Search services should disable public network access

## Mode

`All`

## Description

Disabling public network access improves security by ensuring that your Azure Cognitive Search service is not exposed on the public internet. Creating private endpoints can limit exposure of your Search service.

## Built-In Reference

Modified from: [Search_RequirePublicNetworkAccessDisabled_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Search/Search_RequirePublicNetworkAccessDisabled_Deny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_cognitive_search_services_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_cognitive_search_services_should_disable_public_network_access"
  display_name          = "Azure Cognitive Search services should disable public network access"
  policy_description    = "Disabling public network access improves security by ensuring that your Azure Cognitive Search service is not exposed on the public internet. Creating private endpoints can limit exposure of your Search service."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

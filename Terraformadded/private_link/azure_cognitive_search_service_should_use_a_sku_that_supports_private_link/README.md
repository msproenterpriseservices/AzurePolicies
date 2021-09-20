# Azure Cognitive Search service should use a SKU that supports private link

## Display Name

Azure Cognitive Search service should use a SKU that supports private link

## Mode

`Indexed`

## Description

With supported SKUs of Azure Cognitive Search, Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your Search service, data leakage risks are reduced.

## Built-In Reference

Modified from: [Search_RequirePrivateLinkSupportedResource_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Search/Search_RequirePrivateLinkSupportedResource_Deny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_cognitive_search_service_should_use_a_sku_that_supports_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_cognitive_search_service_should_use_a_sku_that_supports_private_link"
  display_name          = "Azure Cognitive Search service should use a SKU that supports private link"
  policy_description    = "With supported SKUs of Azure Cognitive Search, Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your Search service, data leakage risks are reduced."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

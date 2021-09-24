# Azure Cognitive Search services should use private link

## Display Name

Azure Cognitive Search services should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Azure Cognitive Search, data leakage risks are reduced.

## Built-In Reference

Modified from: [Search_PrivateEndpoints_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Search/Search_PrivateEndpoints_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_cognitive_search_services_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_cognitive_search_services_should_use_private_link"
  display_name          = "Azure Cognitive Search services should use private link"
  policy_description    = "Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Azure Cognitive Search, data leakage risks are reduced."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

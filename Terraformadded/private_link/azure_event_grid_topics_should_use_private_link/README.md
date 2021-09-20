# Azure Event Grid topics should use private link

## Display Name

Azure Event Grid topics should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your Event Grid topic instead of the entire service, you'll also be protected against data leakage risks.

## Built-In Reference

Modified from: [Topics_PrivateEndpoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Event%20Grid/Topics_PrivateEndpoint_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_event_grid_topics_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_event_grid_topics_should_use_private_link"
  display_name          = "Azure Event Grid topics should use private link"
  policy_description    = "Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your Event Grid topic instead of the entire service, you'll also be protected against data leakage risks."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

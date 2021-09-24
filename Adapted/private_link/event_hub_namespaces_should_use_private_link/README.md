# Event Hub namespaces should use private link

## Display Name

Event Hub namespaces should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Event Hub namespaces, data leakage risks are reduced.

## Built-In Reference

Modified from: [EventHub_PrivateEndpoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Event%20Hub/EventHub_PrivateEndpoint_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "event_hub_namespaces_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "event_hub_namespaces_should_use_private_link"
  display_name          = "Event Hub namespaces should use private link"
  policy_description    = "Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Event Hub namespaces, data leakage risks are reduced."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

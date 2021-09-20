# Azure SignalR Service should use private link

## Display Name

Azure SignalR Service should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your Azure SignalR Service resource instead of the entire service, you'll reduce your data leakage risks.

## Built-In Reference

Modified from: [SignalR_PrivateEndpointEnabled_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/SignalR/SignalR_PrivateEndpointEnabled_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_signalr_service_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_signalr_service_should_use_private_link"
  display_name          = "Azure SignalR Service should use private link"
  policy_description    = "Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to your Azure SignalR Service resource instead of the entire service, you'll reduce your data leakage risks."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

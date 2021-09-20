# Container registries should use private link

## Display Name

Container registries should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network.By mapping private endpoints to your container registries instead of the entire service, you'll also be protected against data leakage risks.

## Built-In Reference

Modified from: [ACR_PrivateEndpointEnabled_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Container%20Registry/ACR_PrivateEndpointEnabled_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "container_registries_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "container_registries_should_use_private_link"
  display_name          = "Container registries should use private link"
  policy_description    = "Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The private link platform handles the connectivity between the consumer and services over the Azure backbone network.By mapping private endpoints to your container registries instead of the entire service, you'll also be protected against data leakage risks."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

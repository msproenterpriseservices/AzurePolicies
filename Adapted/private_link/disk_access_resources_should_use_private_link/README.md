# Disk access resources should use private link

## Display Name

Disk access resources should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to diskAccesses, data leakage risks are reduced.

## Built-In Reference

Modified from: [DiskAccesses_PrivateEndpoints_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Compute/DiskAccesses_PrivateEndpoints_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "disk_access_resources_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "disk_access_resources_should_use_private_link"
  display_name          = "Disk access resources should use private link"
  policy_description    = "Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to diskAccesses, data leakage risks are reduced."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

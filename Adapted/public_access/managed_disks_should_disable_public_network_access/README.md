# Managed disks should disable public network access

## Display Name

Managed disks should disable public network access

## Mode

`All`

## Description

Disabling public network access improves security by ensuring that a managed disk isn't exposed on the public internet. Creating private endpoints can limit exposure of managed disks.

## Built-In Reference

Modified from: [Disks_ExportLimitNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Compute/Disks_ExportLimitNetworkAccess_Audit.json)


Terraform azpolicy_definition module usage
-----

```hcl
module "managed_disks_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "managed_disks_should_disable_public_network_access"
  display_name          = "Managed disks should disable public network access"
  policy_description    = "Disabling public network access improves security by ensuring that a managed disk isn't exposed on the public internet. Creating private endpoints can limit exposure of managed disks."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

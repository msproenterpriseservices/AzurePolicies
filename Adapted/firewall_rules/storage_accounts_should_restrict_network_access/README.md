# Storage accounts should restrict network access

## Display Name

Storage accounts should restrict network access

## Mode

`Indexed`

## Description

Network access to storage accounts should be restricted. Configure network rules so only applications from allowed networks can access the storage account. To allow connections from specific internet or on-premises clients, access can be granted to traffic from specific Azure virtual networks or to public internet IP address ranges

## Built-In Reference

Modified from: [Storage_NetworkAcls_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Storage/Storage_NetworkAcls_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "storage_accounts_should_restrict_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "storage_accounts_should_restrict_network_access"
  display_name          = "Storage accounts should restrict network access"
  policy_description    = "Network access to storage accounts should be restricted. Configure network rules so only applications from allowed networks can access the storage account. To allow connections from specific internet or on-premises clients, access can be granted to traffic from specific Azure virtual networks or to public internet IP address ranges"
  policy_category       = "FirewallRules"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

# Azure Event Grid domains should disable public network access

## Display Name

Azure Event Grid domains should disable public network access

## Mode

`All`

## Description

Disabling public network access improves security by ensuring that the resource isn't exposed on the public internet. You can limit exposure of your resources by creating private endpoints instead.

## Built-In Reference

Modified from: [Domains_PublicNetworkAccess_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Event%20Grid/Domains_PublicNetworkAccess_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_event_grid_domains_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_event_grid_domains_should_disable_public_network_access"
  display_name          = "Azure Event Grid domains should disable public network access"
  policy_description    = "Disabling public network access improves security by ensuring that the resource isn't exposed on the public internet. You can limit exposure of your resources by creating private endpoints instead."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

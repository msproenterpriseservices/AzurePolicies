# App Configuration should disable public network access

## Display Name

App Configuration should disable public network access

## Mode

`Indexed`

## Description

Disabling public network access improves security by ensuring that the resource isn't exposed on the public internet. You can limit exposure of your resources by creating private endpoints instead.

## Built-In Reference

Modified from: [PrivateLink_PublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/App%20Configuration/PrivateLink_PublicNetworkAccess_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "app_configuration_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "app_configuration_should_disable_public_network_access"
  display_name          = "App Configuration should disable public network access"
  policy_description    = "Disabling public network access improves security by ensuring that the resource isn't exposed on the public internet. You can limit exposure of your resources by creating private endpoints instead."
  policy_category       = "PublicAccess"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

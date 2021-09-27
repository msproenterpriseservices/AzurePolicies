# Automation accounts should disable public network access

## Display Name

Automation accounts should disable public network access

## Mode

`All`

## Description

Disabling public network access improves security by ensuring that the resource isn't exposed on the public internet. You can limit exposure of your Automation account resources by creating private endpoints instead.

## Built-In Reference

Modified from: [AutomationAccount_PublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Automation/AutomationAccount_PublicNetworkAccess_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "automation_accounts_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "automation_accounts_should_disable_public_network_access"
  display_name          = "Automation accounts should disable public network access"
  policy_description    = "Disabling public network access improves security by ensuring that the resource isn't exposed on the public internet. You can limit exposure of your Automation account resources by creating private endpoints instead."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

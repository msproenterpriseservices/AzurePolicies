# Public network access should be disabled for Batch accounts

## Display Name

Public network access should be disabled for Batch accounts

## Mode

`All`

## Description

Disabling public network access on a Batch account improves security by ensuring your Batch account can only be accessed from a private endpoint.

## Built-In Reference

Modified from: [Batch_DisablePublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Batch/Batch_DisablePublicNetworkAccess_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "public_network_access_should_be_disabled_for_batch_accounts" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "public_network_access_should_be_disabled_for_batch_accounts"
  display_name          = "Public network access should be disabled for Batch accounts"
  policy_description    = "Disabling public network access on a Batch account improves security by ensuring your Batch account can only be accessed from a private endpoint."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

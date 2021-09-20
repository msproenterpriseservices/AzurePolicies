# Public network access should be disabled for Container registries

## Display Name

Public network access should be disabled for Container registries

## Mode

`All`

## Description

Disabling public network access improves security by ensuring that container registries are not exposed on the public internet. Creating private endpoints can limit exposure of container registry resources.

## Built-In Reference

Modified from: [ACR_PublicNetworkAccess_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Container%20Registry/ACR_PublicNetworkAccess_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "public_network_access_should_be_disabled_for_container_registries" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "public_network_access_should_be_disabled_for_container_registries"
  display_name          = "Public network access should be disabled for Container registries"
  policy_description    = "Disabling public network access improves security by ensuring that container registries are not exposed on the public internet. Creating private endpoints can limit exposure of container registry resources."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

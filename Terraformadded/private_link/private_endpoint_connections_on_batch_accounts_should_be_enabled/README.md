# Private endpoint connections on Batch accounts should be enabled

## Display Name

Private endpoint connections on Batch accounts should be enabled

## Mode

`Indexed`

## Description

Private endpoint connections allow secure communication by enabling private connectivity to Batch accounts without a need for public IP addresses at the source or destination.

## Built-In Reference

Modified from: [Batch_PrivateEndpoints_AuditIfNotExists](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Batch/Batch_PrivateEndpoints_AuditIfNotExists.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "private_endpoint_connections_on_batch_accounts_should_be_enabled" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "private_endpoint_connections_on_batch_accounts_should_be_enabled"
  display_name          = "Private endpoint connections on Batch accounts should be enabled"
  policy_description    = "Private endpoint connections allow secure communication by enabling private connectivity to Batch accounts without a need for public IP addresses at the source or destination."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

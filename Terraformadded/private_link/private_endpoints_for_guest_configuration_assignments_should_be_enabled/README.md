# Private endpoints for Guest Configuration assignments should be enabled

## Display Name

Private endpoints for Guest Configuration assignments should be enabled

## Mode

`All`

## Description

Private endpoint connections enforce secure communication by enabling private connectivity to Guest Configuration for virtual machines. Virtual machines will be non-compliant unless they have the tag, 'EnablePrivateNetworkGC'. This tag enforces secure communication through private connectivity to Guest Configuration for Virtual Machines. Private connectivity limits access to traffic coming only from known networks and prevents access from all other IP addresses, including within Azure.

## Built-In Reference

Modified from: [Azure_PrivateLink_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Guest%20Configuration/Azure_PrivateLink_Deny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "private_endpoints_for_guest_configuration_assignments_should_be_enabled" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "private_endpoints_for_guest_configuration_assignments_should_be_enabled"
  display_name          = "Private endpoints for Guest Configuration assignments should be enabled"
  policy_description    = "Private endpoint connections enforce secure communication by enabling private connectivity to Guest Configuration for virtual machines. Virtual machines will be non-compliant unless they have the tag, 'EnablePrivateNetworkGC'. This tag enforces secure communication through private connectivity to Guest Configuration for Virtual Machines. Private connectivity limits access to traffic coming only from known networks and prevents access from all other IP addresses, including within Azure."
  policy_category       = "PrivateLink"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

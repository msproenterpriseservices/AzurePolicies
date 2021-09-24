# Container registries should not allow unrestricted network access

## Display Name

Container registries should not allow unrestricted network access

## Mode

`Indexed`

## Description

Azure container registries by default accept connections over the internet from hosts on any network. To protect your registries from potential threats, allow access from only specific public IP addresses or address ranges. If your registry doesn't have an IP/firewall rule or a configured virtual network, it will appear in the unhealthy resources.

## Built-In Reference

Modified from: [ACR_NetworkRulesExist_AuditDeny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Container%20Registry/ACR_NetworkRulesExist_AuditDeny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "container_registries_should_not_allow_unrestricted_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "container_registries_should_not_allow_unrestricted_network_access"
  display_name          = "Container registries should not allow unrestricted network access"
  policy_description    = "Azure container registries by default accept connections over the internet from hosts on any network. To protect your registries from potential threats, allow access from only specific public IP addresses or address ranges. If your registry doesn't have an IP/firewall rule or a configured virtual network, it will appear in the unhealthy resources."
  policy_category       = "FirewallRules"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

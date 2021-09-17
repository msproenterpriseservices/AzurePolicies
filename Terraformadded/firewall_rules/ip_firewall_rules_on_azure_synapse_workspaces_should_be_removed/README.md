# IP firewall rules on Azure Synapse workspaces should be removed

## Display Name

IP firewall rules on Azure Synapse workspaces should be removed

## Mode

`All`

## Description

Removing all IP firewall rules improves security by ensuring your Azure Synapse workspace can only be accessed from a private endpoint. This configuration audits creation of firewall rules that allow public network access on the workspace.

## Built-In Reference

Modified from: [SynapseWorkspaceFirewallRules_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Synapse/SynapseWorkspaceFirewallRules_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "ip_firewall_rules_on_azure_synapse_workspaces_should_be_removed" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "ip_firewall_rules_on_azure_synapse_workspaces_should_be_removed"
  display_name          = "IP firewall rules on Azure Synapse workspaces should be removed"
  policy_description    = "Removing all IP firewall rules improves security by ensuring your Azure Synapse workspace can only be accessed from a private endpoint. This configuration audits creation of firewall rules that allow public network access on the workspace."
  policy_category       = "FirewallRules"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

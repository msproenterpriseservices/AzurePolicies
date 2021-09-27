# Azure Synapse workspaces should disable public network access

## Display Name

Azure Synapse workspaces should disable public network access

## Mode

`All`

## Description

Disabling public network access improves security by ensuring that the Synapse workspace isn't exposed on the public internet. Creating private endpoints can limit exposure of your Synapse workspaces.

## Built-In Reference

Modified from: [SynapseWorkspacePublicNetworkAccess_Deny](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Synapse/SynapseWorkspacePublicNetworkAccess_Deny.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "azure_synapse_workspaces_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "azure_synapse_workspaces_should_disable_public_network_access"
  display_name          = "Azure Synapse workspaces should disable public network access"
  policy_description    = "Disabling public network access improves security by ensuring that the Synapse workspace isn't exposed on the public internet. Creating private endpoints can limit exposure of your Synapse workspaces."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

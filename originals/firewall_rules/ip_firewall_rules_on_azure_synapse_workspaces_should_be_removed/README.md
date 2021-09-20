# IP firewall rules on Azure Synapse workspaces should be removed

## Display Name

IP firewall rules on Azure Synapse workspaces should be removed

## Mode

`All`

## Description

Removing all IP firewall rules improves security by ensuring your Azure Synapse workspace can only be accessed from a private endpoint. This configuration audits creation of firewall rules that allow public network access on the workspace.

## Built-In Reference

Modified from: [SynapseWorkspaceFirewallRules_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Synapse/SynapseWorkspaceFirewallRules_Audit.json)
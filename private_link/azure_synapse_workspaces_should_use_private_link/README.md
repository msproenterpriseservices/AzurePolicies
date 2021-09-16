# Azure Synapse workspaces should use private link

## Display Name

Azure Synapse workspaces should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Azure Synapse workspace, data leakage risks are reduced.

## Built-In Reference

Modified from: [SynapseWorkspaceUsePrivateLinks_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Synapse/SynapseWorkspaceUsePrivateLinks_Audit.json)
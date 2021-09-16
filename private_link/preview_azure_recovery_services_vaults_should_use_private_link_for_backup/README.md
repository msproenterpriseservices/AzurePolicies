# [Preview]: Azure Recovery Services vaults should use private link for backup

## Display Name

Preview: Azure Recovery Services vaults should use private link for backup

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Azure Recovery Services vaults, data leakage risks are reduced.

## Built-In Reference

Modified from: [RecoveryServices_PrivateEndpoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Backup/RecoveryServices_PrivateEndpoint_Audit.json)
# [Preview]: Azure Recovery Services vaults should use private link for backup

## Display Name

Preview: Azure Recovery Services vaults should use private link for backup

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Azure Recovery Services vaults, data leakage risks are reduced.

## Built-In Reference

Modified from: [RecoveryServices_PrivateEndpoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Backup/RecoveryServices_PrivateEndpoint_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "preview_azure_recovery_services_vaults_should_use_private_link_for_backup" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "preview_azure_recovery_services_vaults_should_use_private_link_for_backup"
  display_name          = "Preview: Azure Recovery Services vaults should use private link for backup"
  policy_description    = "Azure Private Link lets you connect your virtual network to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to Azure Recovery Services vaults, data leakage risks are reduced."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

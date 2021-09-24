# [Preview]: Azure Key Vaults should use private link

## Display Name

Preview: Azure Key Vaults should use private link

## Mode

`Indexed`

## Description

Azure Private Link lets you connect your virtual networks to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to key vault, you can reduce data leakage risks.

## Built-In Reference

Modified from: [AzureKeyVault_Should_Use_PrivateEndpoint_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Key%20Vault/AzureKeyVault_Should_Use_PrivateEndpoint_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "preview_azure_key_vaults_should_use_private_link" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "preview_azure_key_vaults_should_use_private_link"
  display_name          = "Preview: Azure Key Vaults should use private link"
  policy_description    = "Azure Private Link lets you connect your virtual networks to Azure services without a public IP address at the source or destination. The Private Link platform handles the connectivity between the consumer and services over the Azure backbone network. By mapping private endpoints to key vault, you can reduce data leakage risks."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

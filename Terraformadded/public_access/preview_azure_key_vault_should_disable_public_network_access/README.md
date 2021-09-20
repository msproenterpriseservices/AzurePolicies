# [Preview]: Azure Key Vault should disable public network access

## Display Name

Preview: Azure Key Vault should disable public network access

## Mode

`All`

## Description

Disable public network access for your key vault so that it's not accessible over the public internet. This can reduce data leakage risks.

## Built-In Reference

Modified from: [AzureKeyVaultFirewallEnabled_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Key%20Vault/AzureKeyVaultFirewallEnabled_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "preview_azure_key_vault_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "preview_azure_key_vault_should_disable_public_network_access"
  display_name          = "Preview: Azure Key Vault should disable public network access"
  policy_description    = "Disable public network access for your key vault so that it's not accessible over the public internet. This can reduce data leakage risks."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```

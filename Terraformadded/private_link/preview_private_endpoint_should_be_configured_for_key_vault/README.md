# [Preview]: Private endpoint should be configured for Key Vault

## Display Name

Preview: Private endpoint should be configured for Key Vault

## Mode

`Indexed`

## Description

Private link provides a way to connect Key Vault to your Azure resources without sending traffic over the public internet. Private link provides defense in depth protection against data exfiltration.

## Built-In Reference

Modified from: [AzureKeyVaultPrivateEndpointEnabled_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Key%20Vault/AzureKeyVaultPrivateEndpointEnabled_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "preview_private_endpoint_should_be_configured_for_key_vault" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "preview_private_endpoint_should_be_configured_for_key_vault"
  display_name          = "Preview: Private endpoint should be configured for Key Vault"
  policy_description    = "Private link provides a way to connect Key Vault to your Azure resources without sending traffic over the public internet. Private link provides defense in depth protection against data exfiltration."
  policy_category       = "PrivateLink"
  policy_mode           = "Indexed"
  management_group_name = azurerm_management_group.dev.name
}
```

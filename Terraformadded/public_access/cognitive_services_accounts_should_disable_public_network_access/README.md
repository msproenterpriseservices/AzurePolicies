# Cognitive Services accounts should disable public network access

## Display Name

Cognitive Services accounts should disable public network access

## Mode

`All`

## Description

Disabling public network access improves security by ensuring that Cognitive Services account isn't exposed on the public internet. Creating private endpoints can limit exposure of Cognitive Services account.

## Built-In Reference

Modified from: [CognitiveServices_DisablePublicNetworkAccess_Audit](https://github.com/Azure/azure-policy/blob/master/built-in-policies/policyDefinitions/Cognitive%20Services/CognitiveServices_DisablePublicNetworkAccess_Audit.json)

Terraform azpolicy_definition module usage
-----

```hcl
module "cognitive_services_accounts_should_disable_public_network_access" {
  source = "..//modules/azpolicy_definition"
  policy_name           = "cognitive_services_accounts_should_disable_public_network_access"
  display_name          = "Cognitive Services accounts should disable public network access"
  policy_description    = "Disabling public network access improves security by ensuring that Cognitive Services account isn't exposed on the public internet. Creating private endpoints can limit exposure of Cognitive Services account."
  policy_category       = "PublicAccess"
  policy_mode           = "All"
  management_group_name = azurerm_management_group.dev.name
}
```
